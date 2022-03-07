---
title: Päivitä osapuolen osoitekirja ja yleinen osoitekirja
description: Tässä ohjeaiheessa kuvataan, kuinka kaksoiskirjoitustiedot päivitetään osapuolen ja globaaliin osoitekirjamalliin.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 32128d48bfac195530d70b60e67cfd4921fc001e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941080"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Päivitä osapuolen osoitekirja ja yleinen osoitekirja

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Azure Data Factory -malli](https://aka.ms/dual-write-gab-adf) auttaa päivittämään aiemmin luodun **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-taulun tiedot kaksoiskirjoitusmallin osapuolen ja yleisen osoitekirjamallin avulla. Malli täsmäyttää sekä Finance and Operations- että customer engagement -sovellusten tiedot. Prosessin lopussa luodaan **osapuolen** tietueiden **osapuoli**- ja **yhteyshenkilö** kentät ja liitetään asiakkaan varaushakemusten **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-tietueisiin. .csv-tiedosto (`FONewParty.csv`) luodaan luomaan uudet **osapuoli** tietueet Finance and Operations -sovelluksessa. Tämä ohjeaihe sisältää Data Factory -mallissa käytettävät ohjeet ja tietojen päivittämisen.

Jos mukautuksia ei ole, voit käyttää mallia niin kuin se on. Jos olet muokannut **tiliä**, **yhteyshenkilöä** ja **toimittajaa**, sinun on muokattava mallia seuraavien ohjeiden mukaisesti.

> [!Note]
> Mallin avulla voit päivittää vain **osapuolen** tiedot. Tulevat posti- ja sähköiset osoitteet sisällytetään julkaisuun.

## <a name="prerequisites"></a>Edellytykset

Nämä edellytykset vaaditaan:

+ [Azure-tilaus](https://portal.azure.com/)
+ [Mallin käyttäminen](https://aka.ms/dual-write-gab-adf)
+ Olet aiemmin luotu kaksoiskirjoitusasiakas.

## <a name="prepare-for-the-upgrade"></a>Päivityksen valmistelu

+ **Täysin synkronoitu**: Molemmat ympäristöt ovat täysin synkronoituja **Tilin (Asiakas)**, **Yhteyshenkilön** ja **Toimittajan** kanssa.
+ **Integrointiavaimet**: **Tili (Asiakas)**-, **Yhteyshenkilö**- ja **Toimittaja**-taulut Customer Engagement -sovelluksessa käyttävät valmiita integrointiavaimia. Jos olet mukauttanut integrointiavaimia, mukauta mallia.
+ **Osapuolinumero**: Kaikki päivitettävät **Tili (asiakas)**-, **yhteyshenkilö**- ja **toimittaja**-tietueet saavat **osapuoli** numeron. Tietueet, joissa ei ole **osapuolen** numeroa, ohitetaan. Jos haluat päivittää nämä tietueet, lisää niille **osapuolen** numero ennen päivitysprosessin käynnistämistä.
+ **Järjestelmän käyttökomento**: Ota päivitysprosessin aikana sekä Finance and Operations- että customer engagement -ympäristöt offline-tilaan.
+ **Tilannekuva**: Ota tilannekuvia sekä Finance and Operations- että customer engagement -sovelluksista. Voit tarvittaessa palauttaa edellisen tilan tilannekuvasten avulla.

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
    Dynamics Crm Linked Service_properties_type Properties_username | Dynamics-yhteyden muodostanut käyttäjänimi.

    Lisätietoja on ohjeaiheessa [Resource Manager -mallin manuaalinen luominen jokaiselle ympäristölle](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [linkitetyt palvelun ominaisuudet](/azure/data-factory/connector-dynamics-ax#linked-service-properties) ja [tietojen kopioiminen Azure Data Factoryn avulla](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Tarkista käyttöönoton jälkeen tietojoukot, tietovuo ja data factoryn linkitetty palvelu.

   ![Tietojoukot, tietovuo ja linkitetty palvelu](media/data-factory-validate.png)

11. Siirry kohtaan **Hallitse**. Valitse **Yhteydet**-kohdasta **Linkitetty palvelu**. Valitse **DynamicsCrmLinkedService**. Syötä **Muokkaa linkitettyä palvelua (Dynamics CRM)** -lomakkeeseen seuraavat arvot:

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

1. Lopeta Finance and Operations -sovelluksen avulla seuraava **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-kaksoiskirjoitus.

    + Asiakkaat V3 (accounts)
    + Asiakkaat V3 (yhteyshenkilöt)
    + CDS-kontaktit V2 (yhteyshenkilöt)
    + CDS-kontaktit V2 (yhteyshenkilöt)
    + Toimittajat V2 (msdyn_vendors)

2. Varmista, että kartat on poistettu kohteen `msdy_dualwriteruntimeconfig` taulusta Dataversessä.

3. Asenna [kaksoskirjoituksen osapuoli ja yleisiä osoitekirjaratkaisuja](https://aka.ms/dual-write-gab) AppSourcesta.

4. Jos seuraavat taulut sisältävät tietoja Finance and Operations -sovelluksessa, suorita niiden **ensimmäinen synkronointi**.

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

    ![Käynnistimen suoritus](media/data-factory-trigger.png)

    > [!NOTE]
    > Jos olet muokannut **tiliä**, **yhteyshenkilöä** ja **toimittajaa**, sinun on muokattava mallia.

8. Tuo Finance and Operations -sovelluksen uudet **osapuoli**-tietueet.

    + Lataa `FONewParty.csv`-tiedosto Azure blob-objektisäilöstä. Polku on `partybootstrapping/output/FONewParty.csv`.
    + Muunna `FONewParty.csv`-tiedosto Excel-tiedostoksi ja tuo Excel-tiedosto Finance and Operations -sovellukseen.  Jos csv-tuonti toimii sinulle, voit tuoda csv-tiedoston suoraan. Tuonti saattaa kestää muutamia tunteja sen mukaan, mikä tietomäärä on käytössä. Lisätietoja on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../data-import-export-job.md).

    ![Dataverse-osapuolen tietueiden tuominen](media/data-factory-import-party.png)

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

    ![Seuranta-välilehti](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Lisätietoja mallista

Malliin lisättyjä kommentteja löydät [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)-tiedostosta.