---
title: Mukautetun tallennussijainnin määrittäminen luoduille asiakirjoille
description: Tässä ohjeaiheessa käsitellään sähköisten raportointimuotojen muodostamien asiakirjojen tallennussijaintiluettelon laajentamista.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5e9afad936a353c8db3c316ad45c4ce28d33b129
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680803"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Mukautetun tallennussijainnin määrittäminen luoduille asiakirjoille

[!include[banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) kehyksen ohjelmointirajapinnan avulla voit laajentaa ER-muotojen muodostamien asiakirjojen tallennussijaintien luetteloa. Tässä ohjeaiheessa on niiden päätehtävien yleiskatsaus, jotka on tehtävä, jotta mukautettu tallennussijainti voidaan lisätä.

## <a name="prerequisites"></a>Edellytykset

Käyttöön on otettava jatkuvaa koontia tukeva topologia. (Lisätietoja on kohdassa [Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Sinulla on oltava tämän topologian käyttöoikeus jollakin seuraavista rooleista:

- Sähköisen raportoinnin kehittäjä
- Sähköisen raportoinnin toiminnallinen konsultti
- Järjestelmänvalvoja

Tarvitset myös tämän topologian kehitysympäristön käyttöoikeuden.

## <a name="create-or-import-an-er-format-configuration"></a>ER-muotokokoonpanon luonti tai tuonti

[Luo uusi ER-muoto](tasks/er-format-configuration-2016-11.md) nykyisessä topologiassa ja muodosta asiakirjoja, joille aiot lisätä mukautetun tallennussijainnin. Vaihtoehtoisesti voit [tuoda aiemmin luodun ER-muodon tähän topologiaan](general-electronic-reporting-manage-configuration-lifecycle.md).

![Muodon suunnittelutoiminto -sivu](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> Luotavassa tai tuotavassa ER-muodossa on oltava vähintään yksi seuraavista muotoelementeistä:
>
> - Tiedosto
> - Kansio
> - Yhdistystoiminto
> - Liite

## <a name="create-a-new-document-type"></a>Uuden tiedostotyypin luominen

ER-muodon luomien asiakirjojen reitityksen määrittämistä varten on määritettävä [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md). Jokaisessa ER-kohteessa, joka on määritetty tallentamaan muodostetut asiakirjat tiedostoina, on määritettävä tiedoston hallintakehyksen asiakirjatyyppi. Eri asiakirjatyyppejä voidaan käyttää reitittämään eri ER-muotojen muodostamia asiakirjoja.

1. Lisää aiemmin luodulle tai tuodulle ER-muodolle uusi [asiakirjatyyppi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management). Seuraavassa kuvassa asiakirjan tyyppi on **FileX**.
2. Voit erottaa tämän asiakirjatyypin muista asiakirjatyypeistä sisällyttämällä tietyn avainsanan sen nimeen. Esimerkiksi seuraavassa kuvassa nimi on **(PAIKALLINEN) kansio**.
3. Määritä **Luokka**-kentässä **Liitä tiedosto**.
4. Määritä **Ryhmä**-kentässä **Tiedosto**.

![Asiakirjatyypit-sivu](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Asiakirjatyypit ovat yrityskohtaisia. Jos haluat käyttää ER-muotoa, jossa on määritetty kohde, useissa yrityksissä, kullekin yritykselle on määritettävä oma asiakirjatyyppi.

## <a name="review-source-code"></a>Lähdekoodin tarkastelu

Tarkastele **ERDocuManagement**-luokan **insertFile()**-menetelmän koodia. Huomaa, että **AttachingFile()**-tapahtuma muodostetaan, kun muodostettua tiedostoa liitetään tietueeseen.


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

**AttachingFile()**-tapahtuma muodostetaan, kun seuraavat ER-kohteet käsitellään:

- **Arkisto** – Kun tätä kohdetta käytetään, suoritettavan ER-muodon uusi tietue luodaan ERFormatMappingRunJobTable-taulukossa. Tämän tietueen **Arkistoitu**-kentän arvoksi määritetään **Epätosi**. Jos ER-muodon suorittaminen onnistuu, muodostettu asiakirja liitetään tähän tietueeseen ja **AttachingFile()**-tapahtuma muodostetaan. Tässä ER-kohteessa valittu asiakirjatyyppi määrittää liitetyn tiedoston tallennussijainnin (Microsoft Azuren tallennus tai Microsoft SharePoint -kansio).
- **Työarkisto** – Kun tätä kohdetta käytetään, suoritettavan ER-muodon uusi tietue luodaan ERFormatMappingRunJobTable-taulukossa. Tämän tietueen **Arkistoitu**-kentän arvoksi määritetään **Tosi**. Jos ER-muodon suorittaminen onnistuu, muodostettu asiakirja liitetään tähän tietueeseen ja **AttachingFile()**-tapahtuma muodostetaan. ER-parametreissa määritetty asiakirjatyyppi määrittää liitetyn tiedoston tallennussijainnin (Azuren tallennus tai SharePoint-kansio).

![Sähköisen raportoinnin parametrit -sivu](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>ER-kohteen määrittäminen

1. Määritä luodun tai tuodun ER-muodon yhden edellä mainitun elementin (tiedosto, kansio, yhdistämistoiminto tai liite) arkistokohde. Lisätietoja on kohdassa [ER Kohteiden määrittäminen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Käytä asiakirjatyyppiä, jonka lisäsit määritetylle kohteelle aiemmin. (Tämä ohjeaiheen esimerkissä asiakirjatyyppi on **FileX**.)

![Kohdeasetukset-valintaikkuna](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Lähdekoodin muokkaaminen

1. Lisää uusi luokka Microsoft Visual Studio -projektiin ja kirjoita koodi, joka tilaa aiemmin mainitun **AttachingFile()**-tapahtuman. (Lisätietoja käytettävästä laajennettavuusmallista on kohdassa [Vastaaminen käyttämällä kohdetta EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Kirjoita esimerkiksi uudessa luokassa koodia, joka suorittaa seuraavat toiminnot:

    1. Tallenna muodostetut tiedostot sen palvelimen paikallisen tiedostojärjestelmän kansioon, joka suorittaa Application Object Server (AOS) -palvelun.
    2. Tallenna muodostetut tiedostot vain, kun uutta asiakirjatyyppiä (kuten **FileX**-tyyppi, jonka nimessä on avainsana (PAIKALLINEN)) käytetään liitettäessä tiedostoa tietueeseen ER-suoritustyölokissa.

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. Muodosta projekti uudelleen.

## <a name="run-the-er-format-that-you-created-or-imported"></a>Luodun tai tuodun ER-muodon suorittaminen

1. Suorita luotu tai tuotu ER-muoto.
2. Valitse **Organisaation hallinto \> Sähköinen raportointi \> Sähköisen raportoinnin työt**. Etsi tälle suoritustyölle luotu tietue, johon on liitetty muodostettu tiedosto.
3. Etsi sama muodostettu tiedosto paikallisesta **C:\\0**-kansiosta.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)
- [Laajennettavuuden kotisivu](../extensibility/extensibility-home-page.md)
