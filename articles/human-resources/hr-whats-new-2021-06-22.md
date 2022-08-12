---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet 22.6.2021
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 22. kesäkuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61c457abf87ce2da554ddb1472512416159c4dca
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068421"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet 22.6.2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai tulevia toimintoja.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.4258.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Ilmoita käyttäjille työntekijöistä, joilla ei ole työsuhdetoimintoa - Kun lisäkäyttö on käytössä ja kun **Näytä kaikki työntekijät, joilla ei ole työsuhdetta** on poistettu käytöstä ominaisuudenhallinnassa, työntekijöissä, joilla ei ole työsuhdetta näkyy lippu. Lippu ohjaa käyttäjän ottamaan käyttöön **Näytä kaikki työntekijät ilman työsuhdetta** -toiminnon. | Ei käytettävissä| [Työntekijät, joilla ei työsuhdetta](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Etujen hallinnan kelpoisuussääntöjen mukautettujen kenttien tuki | [Mukautetun kentän tuki kelpoisuuskäsittelylle](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Oikeutussääntöjen määrittäminen](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Loman jaksotustapahtuman tarkistus | Ei käytettävissä | [Loman jaksotustapahtuman tarkistus](hr-leave-and-absence-accrue.md)|
| Loma- ja poissaolotyönkulun parannukset | [Loma- ja poissaolotyönkulun parannukset](https://go.microsoft.com/fwlink/?linkid=2147528) | [Pyydä vapaata](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän artikkelin päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ongelman numero | Ongelma |  Kuvaus |
| --- | --- | --- |
| 583052 | Palautteen vastaanottava käyttäjä pystyy muokkaamaan vastaanotettua palautetta | Kun työntekijä saa palautetta suorituskykykirjauskansiosta, hän valitsee **Lisää ulkoinen linkki** -lomakkeesta muokkaamisen. Lomakkeen avulla työntekijä voi muokata saamiaan suorituskykypalautteita. |
| 522281 | Työntekijöiden lukumäärän valitseminen kompensaationhallinnan kompensaatiorakenneruuduissa johtaa vääriin tuloksiin| Kun poraudutaan kompensaatiosuunnitelmiin kompensaatiotyötilasta, näytössä näkyy nyt oikea määrä työntekijöitä. |
| 580683 | Työntekijä- ja esimiesrooleille määritetyt käyttäjät eivät voi liittää huomautuksia tai päivittää suorituskykykirjauskansiota | Työntekijä- ja esimiesrooleille määritetyt käyttäjät eivät voi liittää huomautuksia tai päivittää suorituskykykirjauskansiota. Käyttäjä saa virhesanoman, "Tietuetta ei voi luoda suorituskirjauskansion merkinnässä (HcmPerfJournal). Suojauskäytännön käyttö estetty." |
| 583077 | Työntekijän syntymäpäivä yrityksen loma- ja poissaolokalenterissa näyttää virheellisen päivämäärän | Käyttäjät voivat tarkastella työntekijöiden oikeaa syntymäpäivää yrityksen loma- ja poissaolokalenterissa. |
| 586996 | Yritystenväliset lomanäkymät -toiminto aiheuttaa saldojen tyhjän käytön, kun käyttö on rajoitettu yhteen yritykseen | Käyttäjät voivat tarkastella työntekijän tulevia lomasaldoja oikein, kun yritystenväliset lomanäkymät ovat käytössä. |
| 581014 | Yritystenvälisen loma- ja poissaolonäkymän ottaminen käyttöön aiheuttaa virheen tarkasteltaessa tulevia saldoja | Virheet siitä, kun käyttäjät olivat tarkastelemassa tulevia lomasaldoja, joissa yritystenvälinen lomanäkymä on käytössä, on korjattu. |
| 509404 | Osaston henkilöstölaskenta, jossa ei huomioida työntekijöiden liikkumista osastojen välillä. | Kun työntekijä siirtyy osastolta toiselle, osaston henkilöstömäärä ei vastaa vanhaa osastoa, josta työntekijä on vaihdettu, jos toimen tiedot ovat vanhentuneet kuluvana vuonna. |
| 584851 | Edun hyvityksen suhteellisen jaon sääntö "Ei mitään" ei anna koskaan hyvitystä |Liukuman hyvityksen suhteellisen jaon säännön "Ei mitään" seurauksena työntekijät saavat nolla hyvitystä etukaudella riippumatta siitä, milloin heidät palkattiin. Tämä on ollut kiinteä, jotta työntekijä saa täydet liukumahyvitykset, jos hänet palkataan ennen etukauden alkamista ja ei mitään, jos hänet palkataan kauden alkamisen jälkeen. |
| 584897 | Käytä ulkoisia perusominaisuuksia -toiminnon kopiointi aiheuttaa virheen | Kun yrität tehdä Käytä ulkoisia perusominaisuuksia -tehtävän kaksoiskappaleen, käyttäjä saa virheen "Ei löytänyt objektia, jolla on tunnus UserDefinedAppHostDialogView." |
| 575692 | Loman ja poissaolon jaksottaminen ei ole käytettävissä odottavien työntekijöiden osalta | Loman ja poissaolon jaksotus voidaan suorittaa tuleville palkkauksille, kun **Tehostettu työntekijöiden kirjaus** on otettu käyttöön. |
| 580110 | Yrityksen lisääminen palkanlaskentaintegraatioon palauttaa integraation käyttämään kaikkia entiteettejä, vaikka asetus olisi asetettu olemaan päivittämättä projektia | Jos asiakas on poistanut entiteetit tai muuttanut palkanlaskennan integroinnin tietoprojektia ja on määrittänyt asetuksen, joka estää projektin automaattisen päivityksen, uuden yrityksen lisääminen integrointiin ohittaa asetuksen ja päivittää projektin.  |
| 584518 |Suorituskykyyn liittyminen ja etujen rekisteröiminen | Tämä virhe korjasi suorituskykyongelmia vanhojen etujen rekisteröintiprosessissa. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Ota käyttöön palkanlaskennan yksinkertaistettu integrointi (Palkanlaskennan integroinnin ohjelmointirajapinnat) | [Yksinkertaisen integroinnin käyttöönotto palkanlaskennan palveluntarjoajien kanssa](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palkanlaskennan integroinnin ohjelmointirajapinta](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Tulossa pian

| Ominaisuus | Lisätietoja |
| --- | --- |
| Platform Update 10.0.19 (43) | Ympäristön päivitys 10.0.19 on ajoitettu alkamaan julkaisun kanssa 28.6.2021. Lisätietoja on [Talous- ja toimintosovellusten version 10.0.19 käyttöympäristön päivityksissä (kesäkuu 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19). |
|  Palveluvuosien näytön vaihto | Tämän ominaisuuden avulla voit käyttää eri päivämääriä **Tehostaa työntekijän merkintä** -lomakkeessa ja **Henkilöt**-lomakkeessa näkyvien huollon vuosien laskemiseen.  Tämä on käytettävissä henkilöstöhallinnon parametreissa. |
|  Poissaolojen hallinnan esimiehen käyttöön ottaminen | [Poissaolojen hallinnan esimiehen käyttöön ottaminen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Tiettyjen lomatyyppien liitteiden määrittäminen | Tämän ominaisuuden avulla järjestelmänvalvojat voivat lisätä valtakirjaliitteet, kun tietyn lomatyypin lomapyyntöjä lähetetään. |
|  Määritä lomayksiköt lomatyypin mukaan | Tämän toiminnon avulla järjestelmänvalvojat voivat määrittää lomayksiköt (tunnit tai päivät) kullekin lomatyypille.  |
| Merkitse työntekijät valmiiksi maksettavaksi | [Merkitse työntekijät valmiiksi maksettavaksi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

