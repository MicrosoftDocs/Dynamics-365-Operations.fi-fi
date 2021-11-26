---
title: Päivitä osapuolen osoitekirja ja yleinen osoitekirja
description: Tässä ohjeaiheessa kuvataan, kuinka kaksoiskirjoitustiedot päivitetään osapuolen ja globaaliin osoitekirjamalliin.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 6ed2a8a06b9a026a47ee8bee62aeb63bd64291ef
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783061"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Päivitä osapuolen osoitekirja ja yleinen osoitekirja

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Microsoft Azure Data Factory -malli](https://aka.ms/dual-write-gab-adf) auttaa päivittämään aiemmin luodun **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-taulun tiedot kaksoiskirjoitusmallin osapuolen ja yleisen osoitekirjamallin avulla. Malli täsmäyttää sekä finance and operations- että customer engagement -sovellusten tiedot. Prosessin lopussa luodaan **osapuolen** tietueiden **osapuoli**- ja **yhteyshenkilö** kentät ja liitetään asiakkaan varaushakemusten **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-tietueisiin. .csv-tiedosto (`FONewParty.csv`) luodaan luomaan uudet **osapuoli**-tietueet finance and operations -sovelluksessa. Tämä ohjeaihe sisältää Data Factory -mallissa käytettävät ohjeet ja tietojen päivittämisen.

Jos mukautuksia ei ole, voit käyttää mallia niin kuin se on. Jos olet muokannut **tiliä**, **yhteyshenkilöä** ja **toimittajaa**, sinun on muokattava mallia seuraavien ohjeiden mukaisesti.

> [!NOTE]
> Malli päivittää vain **osapuolen** tiedot. Tulevat posti- ja sähköiset osoitteet sisällytetään julkaisuun.

## <a name="prerequisites"></a>Edellytykset

Seuraavien edellytysten on täytyttävä osapuolen ja yleisen osoitekirjamallin päivittämisessä:

+ [Azure-tilaus](https://portal.azure.com/)
+ [Mallin käyttäminen](https://aka.ms/dual-write-gab-adf)
+ Sinun tulee olla aiemmin luotu kaksoiskirjoitusasiakas.

## <a name="prepare-for-the-upgrade"></a>Päivityksen valmistelu
Päivitystä varten tarvitaan seuraavat tehtävät:

+ **Täysin synkronoitu**: Molemmat ympäristöt ovat täysin synkronoituja **Tilin (Asiakas)**, **Yhteyshenkilön** ja **Toimittajan** kanssa.
+ **Integrointiavaimet**: **Tili (Asiakas)**-, **Yhteyshenkilö**- ja **Toimittaja**-taulut Customer Engagement -sovelluksessa käyttävät valmiita integrointiavaimia. Jos olet mukauttanut integrointiavaimia, mukauta mallia.
+ **Osapuolinumero**: Kaikki päivitettävät **Tili (asiakas)**-, **yhteyshenkilö**- ja **toimittaja**-tietueet saavat **osapuoli** numeron. Tietueet, joissa ei ole **osapuolen** numeroa, ohitetaan. Jos haluat päivittää nämä tietueet, lisää niille **osapuolen** numero ennen päivitysprosessin käynnistämistä.
+ **Järjestelmän käyttökomento**: Ota päivitysprosessin aikana sekä finance and operations- että customer engagement -ympäristöt offline-tilaan.
+ **Tilannekuva**: Ota tilannekuvia sekä finance and operations- että customer engagement -sovelluksista. Voit tarvittaessa palauttaa edellisen tilan tilannekuvasten avulla.

## <a name="deployment"></a>Käyttöönotto

1. Lataa malli [Dynamics-365-FastTrack-käyttöönotto-käyttöomaisuus](https://aka.ms/dual-write-gab-adf) -kentästä.

2. Kirjaudu [Microsoft Azure -palveluun](https://portal.azure.com/).

3. [Resurssiryhmän](/azure/azure-resource-manager/management/manage-resource-groups-portal) luonti.

4. Luo [tallennustili](/azure/storage/common/storage-account-create?tabs=azure-portal) luomallesi resurssiryhmälle.

5. Luo [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) yllä luomallesi resurssiryhmälle.

6. Avaa Data Factory ja valitse **Tee & valvo** -ruutu.

7. Valitse **Hallinta**-välilehdestä **ARM-malli**.

8. Tuo **osapuolen** malli valitsemalla **Tuo ARM -malli**.

9. Tuo malli data factoryyn. Määritä seuraavat arvot **projektitietoja** ja **esiintymän tietoja** varten.

    Kenttä | Arvo
    ---|---
    Tilaus | Azure-tilaus
    Resurssiryhmä | Anna sama resurssi, jolle tallennustili luodaan.
    Alue | Määritä alue.
    Tehtaan nimi | Määritä tehtaan nimi.
    FO-yhdistetyn palvelun pääavain | Määritä sovelluksen avain.
    Azure Blob-objektisäilön yhteysmerkkijonot | Azure Blob-objektisäilön yhteysmerkkijonot.
    Dynamics Crm:n linkitetty palvelusalasana | Käyttäjäksi määritetyn käyttäjätilin salasana.
    FO Linked Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO Linked Service_properties_type Properties_tenant | Määritä vuokraajan tiedot (toimialueen nimi tai vuokraajan tunnus), jota hakemuksesi käyttää.
    FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO Linked Service_properties_type Properties_service Principal Id | Määritä sovelluksen asiakkaan tunnus.
    Dynamics Crm Linked Service_properties_type Properties_username | Dynamics 365 -yhteyden muodostanut käyttäjänimi.

    Lisätietoja on seuraavissa aiheissa: 
    
    - [Resource Manager -mallin manuaalinen luominen kullekin ympäristölle](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Linkitetyt huollon ominaisuudet](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Tietojen kopioiminen Azure Data Factoryn avulla](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Tarkista käyttöönoton jälkeen tietojoukot, tietovuo ja data factoryn linkitetty palvelu.

   ![Tietojoukot, tietovuo ja linkitetty palvelu.](media/data-factory-validate.png)

11. Siirry kohtaan **Hallitse**. Valitse **Yhteydet**-kohdasta **Linkitetty palvelu**. Valitse **DynamicsCrmLinkedService**. Syötä **Muokkaa linkitettyä palvelua (Dynamics CRM)** -lomakkeeseen seuraavat arvot.

    Kenttä | Arvo
    ---|---
    Nimi | DynamicsCrmLinkedService
    kuvaus | Linkitetyt palvelut, jotka yhdistetään CRM-instanssiin yksikkötietojen hakemista varten
    Yhdistä integroinnin suorituspalvelun kautta | AutoResolvelntegrationRuntime
    Käyttöönottotyyppi | Yhdistetty
    Palvelu-Uri | `https://<organization-name>.crm[x].dynamics.com`
    Todennustyyppi | Office365
    Käyttäjänimi |
    Salasana tai Azure Key Vault | Salasana
    Salasana |

## <a name="run-the-template"></a>Suorita malli

1. Lopeta Finance and Operations -sovelluksen avulla seuraava **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-kaksoiskirjoituksen yhdistelmä.

    + Asiakkaat V3 (accounts)
    + Asiakkaat V3 (yhteyshenkilöt)
    + CDS-kontaktit V2 (yhteyshenkilöt)
    + CDS-kontaktit V2 (yhteyshenkilöt)
    + Toimittajat V2 (msdyn_vendors)

2. Varmista, että kartat on poistettu kohteen `msdy_dualwriteruntimeconfig` taulusta Dataversessä.

3. Asenna [kaksoskirjoituksen osapuoli ja yleisiä osoitekirjaratkaisuja](https://aka.ms/dual-write-gab) AppSourcesta.

4. Jos seuraavat taulut sisältävät tietoja finance and operations -sovelluksessa, suorita niiden **ensimmäinen synkronointi**.

    + Tervehdykset
    + Henkilökohtaisten luonteenpiirteiden tyypit
    + Loppusanat
    + Yhteyshenkilöiden arvonimet
    + Päätöksentekoroolit
    + Kanta-asiakastasot

5. Poista seuraavat vaiheet käytöstä Customer Engagement -sovelluksessa.

    + Tilin päivitys
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account
    + Yhteyshenkilön päivitys
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact
    + msdyn_party Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party
    + msdyn_vendor Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor

6. Poista seuraavat vaiheet käytöstä Customer Engagement -sovelluksen työnkuluissa:

    + Toimittajien luonti Tilit-taulussa
    + Toimittajien luonti Tilit-taulussa
    + Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa
    + Luo henkilötyyppisiä toimittajia Toimittajat-taulussa
    + Toimittajien päivitys Tilit-taulussa
    + Toimittajien päivitys Toimittajat-taulussa
    + Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa
    + Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa

7. Suorita malli data factoryssä valitsemalla **Käynnistys nyt** seuraavan kuvan mukaisesti. Tämä prosessi saattaa kestää joitakin tunteja tietojen määrän perusteella.

    ![Käynnistimen suoritus.](media/data-factory-trigger.png)

    > [!NOTE]
    > Jos olet muokannut **tiliä**, **yhteyshenkilöä** ja **toimittajaa**, sinun täytyy muokata mallia.

8. Tuo Finance and Operations -sovelluksen uudet **osapuoli**-tietueet.

    + Lataa `FONewParty.csv`-tiedosto Azure blob-objektisäilöstä. Polku on `partybootstrapping/output/FONewParty.csv`.
    + Muunna `FONewParty.csv`-tiedosto Excel-tiedostoksi ja tuo Excel-tiedosto finance and operations -sovellukseen. Jos csv-tuonti toimii sinulle, voit tuoda csv-tiedoston suoraan. Tuonti saattaa kestää muutamia tunteja sen mukaan, mikä tietomäärä on käytössä. Lisätietoja on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../data-import-export-job.md).

    ![Dataverse-osapuolen tietueiden tuominen.](media/data-factory-import-party.png)

9. Ota seuraavat vaiheet käyttöön Customer Engagement -sovelluksissa:

    + Tilin päivitys
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account
    + Yhteyshenkilön päivitys
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact
    + msdyn_party Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party
    + msdyn_vendor Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor

10. Aktivoi seuraavat työnkulut Customer Engagement -sovelluksessa, jos poistat niiden aktivoinnin aiemmissa vaiheissa:

    + Toimittajien luonti Tilit-taulussa
    + Toimittajien luonti Tilit-taulussa
    + Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa
    + Luo henkilötyyppisiä toimittajia Toimittajat-taulussa
    + Toimittajien päivitys Tilit-taulussa
    + Toimittajien päivitys Toimittajat-taulussa
    + Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa
    + Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa

11. Suorita **osapuoliin** liittyvät kartat [osapuolen ja yleisen osoitekirjan](party-gab.md) ohjeiden mukaisesti.

## <a name="troubleshooting"></a>Vianmääritys

1. Jos prosessi epäonnistuu, käynnistä data factory uudelleen epäonnistuneen tehtävän perusteella.
2. Osa tiedostoista luodaan data factoryssa, jota voit käyttää tietojen oikeellisuustarkistusta varten.
3. Data factory suoritetaan pilkuilla erotettujen csv-tiedostojen perusteella. Jos kenttäarvolla on pilkku, se voi sisältää tulokset, mutta ei välttämättä pilkkua. Poista pilkut.
4. **Seuranta**-välilehdessä on tietoja kaikista vaiheista ja käsitellyistä tiedoista. Valitse tietty virheenkorjausvaihe.

    ![Seuranta-välilehti.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Lisätietoja mallista

Mallin lisätiedot ovat ohjeaiheessa [Comments for Azure Data Factor -mallin lueminut-tiedosto](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
