---
title: Invoice Capture -ratkaisun määrittäminen
description: Tässä artikkelissa kerrotaan, miten Invoice Capture -ratkaisu määritetään.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691148"
---
# <a name="configure-the-invoice-capture-solution"></a>Invoice Capture -ratkaisun määrittäminen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kun Invoice Capture -ratkaisu on asennettu, ympäristö on määritettävä. Prosessi koostuu alla mainituista perusvaiheista.

1. **Pakollinen:** Synkronoi yritykset Microsoft Dynamics 365 Financesta. Tämän vaiheen avulla määritetään organisaatiorakenne Microsoft Power Platformissa.
2. **Pakollinen:** Määritä kanavat laskujen kuvien tuontia varten. Ratkaisu tukee seuraavia kanavia:

    - Office 365 Outlook (oletus)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **Valinnainen:** Määritä lisää konfiguraatioryhmiä OCR-tekstintunnistuspalvelua varten.
4. **Valinnainen:** Määritä vastaavuusmäärityksen säännöt yritykselle, toimittajatilille, nimikkeelle ja hankintatyypille.

Tässä artikkelissa käsitellään prosessin kahta pakollista vaihetta. Lisätietoja on konfiguraatioryhmistä on kohdassa [Invoice Capture -ratkaisun konfiguraatioryhmät](invoice-capture-config-group.md). Lisätietoja yhdistämismäärityksen säännöistä on kohdassa [Invoice Capture -ratkaisun yhdistämismäärityksen säännöt](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Yritysten hallinta

Finance määrittää yritykset organisaatioiksi, jotka määritetään viranomaisrekisteröinnin avulla. Liiketoiminnan aktiviteetit suoritetaan ja tallennetaan erillisissä yrityksissä. Microsoft Power Platformissa liiketoimintayksiköt, käyttöoikeusroolit ja käyttäjät linkitetään yhteen tavalla, joka vahvistaa rooliin perustuvan suojausmallin.

Liiketoimintayksiköitä käytetään yhdessä käyttöoikeusroolien kanssa tietojen käyttöoikeuksien hallinnassa. Käyttäjät näkevät vain tiedot, joita he tarvitsevat työssään. Invoice Capture -ratkaisu sisältää määritystilan, jossa on mahdollista ladata Financen olemassa olevien yritysten perustiedot ja hallita näitä manuaalisesti luotuja entiteettejä. Yrityksiä käytetään toimittajan laskuissa ja suojauksen hallinnassa.

Kun yritys luodaan ja kun se näkyy luettelonäkymässä, luodaan automaattisesti oletusliiketoimintayksikkö, jolla on sama nimi. Ryhmälle myönnetään **ostoreskontran käsittelijän** käyttöoikeusrooli. Kun yritykset tuodaan, tuodaan myös Financen peruspäätiedot. Yritys tunnistaa nimikkeet, joita ei ole, ja lisää ne Invoice Capture -ratkaisuun. Uusille yrityksille määritetään oletuskonfiguraatioryhmä.

### <a name="sync-legal-entities"></a>Yritysten synkronoiminen

Yrityksiä ei voi luoda suoraan. Yritykset on kuitenkin mahdollista synkronoida Financesta. Voit synkronoida yritykset alla olevien ohjeiden mukaan.

1. Siirry kohtaan **Asetukset \> Järjestelmäasetukset \> Yritysten hallinta**.
2. Valitse **Synkronoi yritykset** ja valitse sitten **OK** vahvistusikkunassa.

Kun synkronointi on valmis, näytetään uusien yritysten määrä. Uudet yritykset näytetään luettelonäkymässä. Uusille yrityksille määritetään oletuskonfiguraatioryhmä.

## <a name="configure-invoice-import-channels"></a>Laskun tuontikanavien määrittäminen

Toimittajat lähettävät laskuja eri kanavien kautta (sähköposti, tiedostotyötila tai laskuportaali) eri muodoissa (paperi tai kuva). Invoice Capture -ratkaisu voi käsitellä erilaisia kanavia ja muotoja. Seuraavia tyyppejä tuetaan:

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

Kun kanava luodaan tietylle tilille, muodostetaan automaattinen työnkulku, jolla on esimääritetty malli. Se valvoo saapuvia sähköpostiviestejä tai tiedostoja Saapuneet-kansiossa tai -tilassa. Mikä tahansa tiedosto, jolla on voimassa oleva lasku, voidaan tunnistaa ja lähettää laskutusalueelle odottamaan ostoreskontran käsittelijää. Liitteen on oltava PDF- tai kuvamuodossa. Laskut voidaan ladata Invoice Capture -ratkaisuun kanavamäärityksen mukaan.

### <a name="create-a-channel"></a>Kanavan luominen

Jos olet tuonut lisäratkaisupaketin (Dynamics 365 Invoice Capture – asennustyökalut), Office 365 Outlookin oletusyhteys on valmis käytettäväksi. Jos haluat luoda useita yhteyksiä eri sähköpostitileille tai muille kanavatyypeille, katso kohta [Lisäyhteyksien luominen kanaville](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Voit luoda kanavan seuraavien vaiheiden avulla.

1. Siirry kohtaan **Asetukset \> Järjestelmäasetukset \> Määritä kanavat**.
2. Valitse **Uusi**.
3. Määritä seuraavat kentät:

    - Kanavan nimi
    - Kuvaus
    - Tyyppi
    - Yhteys

Ratkaisuun voi tuoda vain sähköpostiviestit ja tiedostot, jotka vastaavat alla olevia ehtoja.

| Tyyppi               | Konfiguraatio  | Lisätietoja |
|--------------------|----------------|------------------|
| Office 365 Outlook | Kansio         | Sähköpostikansion on oltava juurihakemistossa. Oletusarvoisesti käytetään Saapuneet-kansiota. Alikansiota ei tueta. |
|                    | Aihesuodatin | (Valinnainen) Alimerkkijono, joka lisätään aiheeseen. |
|                    | Alkaen           | (Valinnainen) Lähettäjän sähköpostiosoite tai lähettäjien sähköpostiosoitteet. Jos haluat määrittää useita osoitteita, käytä puolipistettä (;) erottimena. |
| SharePoint         | Sivuston osoite   | Sivuston osoitteen URL-osoite. |
|                    | Kansio         | Sivuston osoitteen kansio. |

### <a name="activate-the-channel"></a>Kanavan aktivoiminen

Kun työnkulku tallennetaan, kentissä näkyy kanavan tila sekä aika, jolloin kanava luotiin. Aluksi **Tila**-kentän arvoksi määritetään **Passiivinen**. **Tilan syy** -kenttä osoittaa, että kanava on alustettu ja se voidaan aktivoida.

Aktivoi kanava valitsemalla **Aktivoi**. **Tila**- ja **Tilan syy** -kentät päivitetään.

Jos kanava ei ole pakollinen, voit poistaa sen aktivoinnin. Jos haluat poistaa kanavan aktivoinnin, valitse **Poista aktivointi**. **Tila**- ja **Tilan syy** -kentät päivitetään.

### <a name="manage-flows-in-flow-management"></a>Työnkulkujen hallinta työnkulkujen hallinnassa

Voit tarkastella kanavaa **Määritä kanavat** -sivulla tai työnkulkujen hallinnassa.

Voit tarkastella lisätietoja siirtymällä kohtaan **Hallintajärjestelmä \> Oletusratkaisu \> Pilvityönkulut** ja valitsemalla kohdetyönkulku. Näkyvissä ovat esimerkiksi linkitetyt yhteydet, omistajat ja suoritushistoria.

Jos haluat synkronoida tilan, valitse **Tarkista** ja vahvista, että kanavan tila vastaa työnkulun tilaa.

Jotkin poikkeusten käsittelyn tapaukset näkyvät **Tilan syy** -kentässä seuraavasti:

- **Puuttuva Dataverse-yhteys** – Nykyinen käyttäjä ei ole luonut vähintään yhtä **Microsoft Dataverse** -yhteysviitettä.
- **Ei löydy** – Kanavaan linkitetty työnkulku on poistettu työnkulkujen hallinnassa. Kanava tulee tallentaa uudelleen uuden kanavan luomista varten.
- **Aktivointi on poistettu työnkulkujen hallinnassa** – Työnkulun aktivointi on poistettu työnkulkujen hallinnassa, ja kanavan tila on eri kuin työnkulkujen tila.
- **Aktivoitu työnkulkujen hallinnassa** – Työnkulku on aktivoitu työnkulkujen hallinnassa, ja kanavan tila on eri kuin työnkulkujen tila.
- **Odottamaton virhe** – Käyttäjän on vahvistettava, että sivusto on Yhteyssivusto, ja että kansio on Asiakirjakirjasto.
