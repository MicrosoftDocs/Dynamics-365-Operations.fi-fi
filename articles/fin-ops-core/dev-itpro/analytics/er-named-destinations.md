---
title: Tulostuksenhallinnan tietuekohtaisten ER-kohteiden määrittäminen
description: Tässä artikkelissa käsitellään lähtevien asiakirjojen luontia varten määritetyn sähköisen raportoinnin (ER) tulostuksenhallinnan tietuekohtaisten kohteiden määrittämistä.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2972dc6a0b373cbc63b811c01ef7a5538810edbb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872710"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Tulostuksenhallinnan tietuekohtaisten ER-kohteiden määrittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten käyttäjä voi suorittaa järjestelmänvalvojan tai myyntireskontran käsittelijän roolissa seuraavat tehtävät:

- Vapaatekstilaskuja luovan ER-ratkaisun nimettyjen [sähköisen raportoinnin (ER)](general-electronic-reporting.md) kohteiden määrittäminen.
- ER-kohteen määrittäminen yhdelle [tulostuksenhallinnan](document-reporting-services.md) tietueelle.

Menettelyt voidaan suorittaa USMF-yrityksessä. Koodausta ei tarvita.

## <a name="introduction"></a>Johdanto

[Kohteet](electronic-reporting-destinations.md) voidaan määrittää kullekin ER-[muodon](general-electronic-reporting.md) [määrityksen](general-electronic-reporting.md#Configuration) tiedostotulosteosan kansiolle, jolla luodaan lähtevä asiakirja. Kun tämän tyyppinen ER-muoto suoritetaan ja jos käytössä on soveltuvat käyttöoikeudet, myös määritettyjä kohdeasetuksia voidaan muuttaa suorituksen aikana.

Microsoft Dynamics 365 Financen **versiossa 10.0.17 ja sitä uudemmissa versioissa** ER-muodolle voidaan [määrittää](er-apis-app10-0-17.md) toimintokoodi määrittämään toiminto, jonka käyttäjät suorittavat suorittamalla ER-muodon. Esimerkiksi **Myyntireskontra**-moduulin tulostuksen hallinta-asetuksissa voidaan valita ER-muoto, joka luo tietyn liiketoiminta-asiakirjan, kuten vapaatekstilaskun. Lasku voidaan sitten esikatsella valitsemalla **Näytä** tai lähettää tulostimeen valitsemalla **Tulosta**. Jos toiminto siirretään suoritettavaan ER-muotoon suorituksen aikana, [eri käyttäjän toimien eri ER-kohteita voidaan määrittää](er-action-dependent-destinations.md).

Financen **versiossa 10.0.21 ja sitä uudemmissa versioissa**, ER-muodolle voidaan [määrittää](er-apis-app10-0-21.md) nimetty koodi, joka voidaan sitten määrittää ER-muotoa suoritettaessa käsiteltävään tulostuksenhallintatietueeseen. Esimerkiksi **Myyntireskontra**-moduulin tulostuksen hallinta-asetuksissa **Alkuperäinen**-tietue määritetään suorittamaan seuraavat toiminnot:

- ER-muotojen suorittaminen.
- Luodun laskun lähettäminen sähköpostitse asiakkaalle.
- **Kopio**-tietueen määrittäminen suorittamaan sama muoto.
- Laskun kopion tulostaminen verkkotulostimeen.

Tässä tapauksessa on määritettävä suoritettavalle ER-muodolle on määritettävä eri ER-kohteet, ja tulostuksenhallinnan eri tietueille on valittava kohteet.

## <a name="prerequisites"></a>Edellytykset

Ennen aloittamista **Salli tulostuksenhallinnan kohdekohtaisten ER-kohteiden määrittäminen** -toiminto on otettava käyttöön [Ominaisuuksien hallinta](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) -työtilassa. Myös lähdekoodia on muutettava, jotta nimettyjä ER-kohteita voidaan määrittää nykyisessä Finance-esiintymässä ja jotta [uusi](er-apis-app10-0-21.md) ER-ohjelmointirajapinta voidaan ottaa käyttöön.

Lisäksi **Vapaatekstilasku (Excel)** -ER-määritys on [tuotava](er-download-configurations-global-repo.md) Finance-esiintymään.

## <a name="configure-a-new-er-destination"></a>Uuden ER-kohteen määrittäminen

1. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
2. Valitse asiakastilin **US-001** lasku.
3. Valitse **Vapaatekstilasku**-sivun **Lasku**-välilehden **Tulostuksenhallinta**-ryhmässä **Tulostuksenhallinta**.
4. Laajenna **Tulostuksenhallinta-asetukset**-sivulla **Moduuli - Myyntireskontra** \> **Asiakirjat** \> **Vapaatekstilasku**, valitse **Alkuperäinen**-tietue ja toimi seuraavasti:

    1.  Katso, mitkä ovat valitun tietueen nykyiset asetukset:
        -   **FreeTextInvoice.Report**-SSRS-oletusraportti on valittu **Raportin muoto** -kentässä.
        -   **Kohde**-kentässä näkyvä **\<Default\>**-nimi ilmaisee, että määritettyyn SSRS-raporttiin ei ole valittu mukautettua kohdetta. 
    2.  Valitse **Raportin muoto** -kentässä **Vapaatekstilasku (Excel)** -ER-muotomääritys.
        -   **Kohde**-kentän nimeksi vaihtuu **Kohteen nimi**.
        -   **Kohteen nimi** -kentässä näkyvä **\<No named destination\>** -nimi ilmaisee, että määritettyyn ER-muotoon ei ole valittu nimettyä kohdetta.
    3.  Valitse nuolipainike **Kohteen nimi** -kentän oikealla puolella.    
    4. Anna **Sähköisen raportoinnin nimetty kohde** -sivun **Nimi**-kenttään **Pääkohde**.
    5. Valitse **Tallenna**.
    6. [Määritä](er-destination-type-email.md) **Tiedostokohde**-pikavälilehdessä **Raportti**-osan **Sähköposti**-kohde.
    7. Sulje **Sähköisen raportoinnin nimetty kohde** -sivu.
    8. Valitse **Tulostuksenhallinta-asetukset**-sivun **Kohteen nimi** -kentässä nimetty **Pääkohde**-kohde.

    ![Valitun ER-muodon nimetyn ER-kohteen määrittäminen ja sen määrittäminen määritettyyn tulostuksenhallintatietueeseen Tulostuksenhallinta-asetukset-sivulla](./media/er-named-destinations-01.gif)

    **Vapaatekstilasku (Excel)** -muodolle on nyt määritetty nimetty **Pääkohde**-ER-kohde ja se on määritetty tulostuksenhallinnan **Alkuperäinen**-tietueeseen kohdassa **Moduuli – myyntireskontra** \> **Asiakirjat** \> **Vapaatekstilasku**.

5. Laajenna **Moduuli – myyntireskontra** \> **Tili – US-001** \> **Vapaatekstilasku**, valitse **Alkuperäinen**-tietue ja toimi seuraavasti:

    1. Pidä tietuetta valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse **Ohita**.
    2. Valitse nuolipainike **Kohteen nimi** -kentän oikealla puolella.
    3. Valitse **Sähköisen raportoinnin nimetty kohde** -sivun toimintoruudussa **Uusi**.
    4. Anna **Nimi**-kenttään **US-001 kohde**.
    5. [Määritä](er-destination-type-print.md) **Tiedostokohde**-pikavälilehdessä **Raportti**-osan **Tulostin**-kohde.
    6. Sulje **Sähköisen raportoinnin nimetty kohde** -sivu.
    7. Valitse **Tulostuksenhallinta-asetukset**-sivun **Kohteen nimi** -kentässä nimetty **US-001 kohde** -kohde.

    ![Valitun ER-muodon nimetyn ER-kohteen määrittäminen ja sen määrittäminen määritettyyn tulostuksenhallintatietueeseen Tulostuksenhallinta-asetukset-sivulla](./media/er-named-destinations-02.gif)

    **Vapaatekstilasku (Excel)** -muodolle on nyt määritetty nimetty **US-001 kohde**-ER-kohde, ja se on määritetty tulostuksenhallinnan **Alkuperäinen**-tietueeseen kohdassa **Moduuli – myyntireskontra** \> **Tili – US-001** \> **Vapaatekstilasku**.

Kun vapaatekstilasku nyt käsitellään, **Vapatekstilasku (Excel)** -ER-muoto suoritetaan, jokin seuraavista tapahtumista tapahtuu:

- Jos vapaatekstilasku on tarkoitettu jollekin muulle asiakkaalle kuin US-001, luotu asiakirja lähetään sähköpostitse.
- Jos vapaatekstilasku on tarkoitettu asiakkaalle US-001, luotu asiakirja tulostetaan.

> [!NOTE]
> Jos suorituksen aikana käsiteltävälle tulostuksenhallintatietueelle ei ole määritetty nimettyä kohdetta, ER-oletuskohteita käytetään, jos ne ovat käytettävissä suoritettavassa ER-muodossa.

> [!IMPORTANT]
> Nimetyt kohteet ilmoitetaan **Sähköisen raportoinnin kohde** -sivulla (**Organisaation hallinta** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin kohde**), jos valitulle ER-muodolle on määritetty ainakin yksi nimetty kohde.
>
> ![Ilmoitus valitun ER-muodon määritetyistä nimetyistä kohteista Sähköisen raportoinnin kohde -sivulla](./media/er-named-destinations-03.png)
>
> Jos oletuskohde poistetaan, myös kaikki nimetyt kohteet poistetaan. Jos kyseiset nimetyt kohteet valittiin tulostuksenhallintatietueisiin, kyseisten nimettyjen kohteiden valinta peruutetaan.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Aiemmin luodun ER-kohteen kopioiminen uutena nimettynä kohteena

Jos ER-muodon käytettävissä on oletusarvoinen nimetty ER-kohde, sitä voidaan käyttää usein ER-kohteiden mallina. Uusi oletuskohteeseen perustuva ER-kohde voidaan luoda valitsemalla **Sähköisen raportoinnin nimetty kohde** -sivulla **Kopioi oletuksesta**. Uuden kohteen nimi on **Oletus**. Tämä vaihe voidaan toistaa niin monta kertaa kuin tarvitaan.

Uuden nimetyn kohteen malliksi voidaan valita mikä tahansa aiemmin luotu nimetty kohde. Uusi valittuun nimettyyn kohteeseen perustuva nimetty ER-kohde voidaan luoda valitsemalla **Sähköisen raportoinnin nimetty kohde** -sivulla **Kopioi**. Uudella kohteella on sama nimi kuin valitulla nimetyllä kohteella, mutta sen nimen loppuun on lisätty Kopio. Tämä vaihe voidaan toistaa niin monta kertaa kuin tarvitaan.

## <a name="security-considerations"></a>Tietojen suojaamisesta

Nimetyt ER-kohteet voidaan määrittää **Tuloksenhallinta-asetukset**-sivulla vain, jos käytössä on siihen tarvittava [käyttöoikeus](../sysadmin/role-based-security.md#permissions). Käyttöoikeus voidaan myöntää, jos **Määritä sähköisen raportoinnin muodon kohde** [-velvollisuus](../sysadmin/role-based-security.md#duties) on määritetty johonkin omaa [käyttöoikeusrooliin](../sysadmin/role-based-security.md#security-roles). Lisätietoja on kohdassa [Huomioonotettavaa suojauksesta](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)

[Sähköisen raportointikehyksen ohjelmointirajapinnan muutokset Application update 10.0.17 -päivitystä varten](er-apis-app10-0-17.md)

[Sähköisen raportointikehyksen ohjelmointirajapinnan muutokset Application update 10.0.21 -päivitystä varten](er-apis-app10-0-21.md)

[Koodin muuttaminen antamaan käyttäjille mahdollisuus määrittää ja käyttää nimettyjä ER-kohteita](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
