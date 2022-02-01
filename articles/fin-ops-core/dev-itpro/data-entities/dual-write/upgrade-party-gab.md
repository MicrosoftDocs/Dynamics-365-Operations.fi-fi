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
ms.openlocfilehash: eaafe8d98049cb8838317396f28e9d6ca720a677
ms.sourcegitcommit: 08dcbc85e372d4e4fb3ba64389f6d5051212c212
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/20/2022
ms.locfileid: "8015712"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Päivitä osapuolen osoitekirjan ja yleisen osoitekirjan malliin

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Microsoft Azure Data Factory -mallien](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) avulla voit päivittää seuraavat aiemmin luodut tiedot kaksoiskirjoituksessa osapuolen ja yleisen osoitekirjan malleissa: **Asiakas**-, **Yhteyshenkilö**- ja **Toimittaja**-taulujen tiedot sekä postiosoitteiden ja sähköisten osoitteiden tiedot.

Seuraavat kolme Data Factory -mallia ovat käytettävissä. Ne auttavat täsmäyttämään sekä rahoitus- ja toiminta -sovellusten että asiakkaiden sitouttamissovellusten tiedot.

- **[Osapuolimalli](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Päivitä tiedot kaksoiskirjoituksen Party-GAB-skeemaan/arm_template.json-tiedostoon)** – Tämä malli auttaa päivittämään **Asiakas**-, **Yhteyshenkilö**- ja **Toimittaja**-tietoihin liittyvät **Osapuoli**- ja **Yhteyshenkilö**-tiedot.
- **[Osapuolen postiosoitemalli](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (Tietojen päivittäminen kaksoiskirjoituksen Party-GAB-skeemaan / Päivitä osapuolen postiosoitteeksi - GAB/arm_template.json)** – Tämän mallin avulla voit päivittää **Asiakas**-, **Yhteyshenkilö**- ja **Toimittaja**-tietoihin liittyvät postiosoitteet.
- **[Osapuolen sähköisen osoitteen malli](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (Tietojen päivittäminen kaksoiskirjoituksen Party-GAB-skeemaan / Päivitä osapuolen sähköiseksi osoitteeksi - GAB/arm_template.json)** – Tämän mallin avulla voit päivittää **Asiakas**-, **Yhteyshenkilö**- ja **Toimittaja**-tietoihin liittyvät sähköiset osoitteet.

Prosessin lopussa luodaan seuraavat pilkuilla erotettujen arvojen (.csv) tiedostot.

| Tiedoston nimi | Tarkoitus |
|---|---|
| FONewParty.csv | Tämä tiedosto auttaa luomaan uudet **osapuoli**-tietueet rahoitus- ja toiminta -sovelluksessa. |
| ImportFONewPostalAddressLocation.csv | Tämän tiedoston avulla voit luoda rahoitus- ja toiminta -sovelluksessa uusia **Postiosoitteen sijainti** -tietueita. |
| ImportFONewPartyPostalAddress.csv | Tämän tiedoston avulla voit luoda rahoitus- ja toiminta -sovelluksessa uusia **Osapuolen postiosoite** -tietueita. |
| ImportFONewPostalAddress.csv | Tämän tiedoston avulla voit luoda rahoitus- ja toiminta -sovelluksessa uusia **Postiosoite**-tietueita. |
| ImportFONewElectronicAddress.csv | Tämän tiedoston avulla voit luoda rahoitus- ja toiminta -sovelluksessa uusia **Sähköinen osoite**-tietueita. |

Tämä aihe sisältää Data Factory -mallin käytön ja tietojen päivittämisen ohjeet. Jos mukautuksia ei ole, voit käyttää malleja sellaisina kuin ne ovat. Jos olet mukauttanut **Asiakas**-, **Yhteyshenkilö**- ja **Toimittaja**-tietoja, sinun on muokattava malleja tämän aiheen ohjeiden mukaisesti.

> [!IMPORTANT]
> On noudatettava erityisohjeita suoritettaessa osapuolen postiosoitteen ja osapuolen sähköisen osoitteen malleja. Sinun on suoritettava ensin osapuolen malli, sitten osapuolen postiosoitemalli ja sitten osapuolen sähköisen osoitteen malli. Kukin malli on suunniteltu tuotavaksi erillisessä datatehtaassa.

## <a name="prerequisites"></a>Edellytykset

Seuraavien edellytysten on täytyttävä, ennen kuin voit päivittää osapuolen mallin ja yleisen osoitekirjamallin:

+ Sinulla on oltava [Azure-tilaus](https://portal.azure.com/).
+ Sinulla on oltava [mallien](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) käyttöoikeus.
+ Sinun tulee olla aiemmin luotu kaksoiskirjoitusasiakas.

## <a name="prepare-for-the-upgrade"></a>Päivityksen valmistelu

Päivitys edellyttää seuraavat valmistelut:

+ **Täysi synkronointi**: Sekä Finance and Operations -ympäristö että Customer Engagement -ympäristö ovat täysin synkronoidussa tilassa **Tili (asiakas)**-, **Yhteyshenkilö**- ja **Toimittaja**-tauluille.
+ **Integrointiavaimet**: **Tili (Asiakas)**-, **Yhteyshenkilö**- ja **Toimittaja**-taulut Customer Engagement -sovelluksissa käyttävät käyttövalmiita integrointiavaimia. Jos olet mukauttanut integrointiavaimia, mukauta mallia.
+ **Osapuolinumero:** Kaikki päivitettävät **Tili (asiakas)**-, **Yhteyshenkilö**- ja **Toimittaja**-tietueet saavat osapuolinumeron. Tietueet, joissa ei ole osapuolen numeroa, ohitetaan. Jos haluat päivittää nämä tietueet, lisää niille osapuolen numero ennen päivitysprosessin käynnistämistä.
+ **Järjestelmän käyttökatko**: Päivitysprosessin aikana sekä Finance and Operations- että Customer Engagement -ympäristöt on siirrettävä offline-tilaan.
+ **Tilannekuva:** Ota tilannekuva sekä rahoitus- ja toiminta- että Customer Engagement -sovelluksista. Voit sitten tarvittaessa palauttaa edellisen tilan tilannevedosten avulla.

## <a name="deployment"></a>Käyttöönotto

1. Lataa mallit [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) -säilöstä.
2. Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).
3. [Resurssiryhmän](/azure/azure-resource-manager/management/manage-resource-groups-portal) luonti.
4. Luo [tallennustili](/azure/storage/common/storage-account-create?tabs=azure-portal) luomallesi resurssiryhmälle.
5. Luo [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) luomallesi resurssiryhmälle.
6. Avaa Data Factory ja valitse **Tee & valvo** -ruutu.
7. Valitse **Hallinta**-välilehdestä **ARM-malli**.
8. Tuo **osapuolen** malli valitsemalla **Tuo ARM -malli**.
9. Tuo malli data factoryyn. Määritä seuraavat arvot **projektitietoja** ja **esiintymän tietoja** varten.

    | Kenttä | Arvo |
    |---|---|
    | Tilaus | Azure-tilaus |
    | Resurssiryhmä | Anna sama resurssi, jonka alla tallennustili luodaan. |
    | Alue | Alue |
    | Tehtaan nimi | Factoryn nimi |
    | FO-yhdistetyn palvelun pääavain | Sovelluksen avain |
    | Azure Blob-objektisäilön yhteysmerkkijonot | Azure Blob -objektisäilön yhteysmerkkijono |
    | Dynamics Crm:n linkitetty palvelusalasana | Käyttäjätunnukseksi määritetyn käyttäjätilin salasana. |
    | FO Linked Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO Linked Service_properties_type Properties_tenant | Sen vuokraajan tiedot (toimialueen nimi tai vuokraajan tunnus), jonka alla sovelluksesi sijaitsee |
    | FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO Linked Service_properties_type Properties_service Principal Id | Sovellusasiakkaan tunnus |
    | Dynamics Crm Linked Service_properties_type Properties_username | Dynamics 365 -yhteyden muodostava käyttäjätunnus |

    Lisätietoja on seuraavissa aiheissa:

    - [Resource Manager -mallin manuaalinen luominen kullekin ympäristölle](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Linkitetyt huollon ominaisuudet](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Tietojen kopioiminen Azure Data Factoryn avulla](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Tarkista käyttöönoton jälkeen tietojoukot, tietovuo ja data factoryn linkitetty palvelu.

    ![Tietojoukot, tietovuo ja linkitetty palvelu.](media/data-factory-validate.png)

11. Siirry kohtaan **Hallinta**. Valitse **Yhteydet**-kohdasta **Linkitetty palvelu**. Valitse sitten **DynamicsCrmLinkedService**. Syötä **Muokkaa linkitettyä palvelua (Dynamics CRM)** -valintaikkunaan seuraavat arvot.

    | Kenttä | Arvo |
    |---|---|
    | Nimi | DynamicsCrmLinkedService |
    | kuvaus | Linkitetyt palvelut, jotka yhdistetään CRM-instanssiin yksikkötietojen hakemista varten |
    | Yhdistä integroinnin suorituspalvelun kautta | AutoResolvelntegrationRuntime |
    | Käyttöönottotyyppi | Yhdistetty |
    | Palvelu-Uri | `https://<organization-name>.crm[x].dynamics.com` |
    | Todennustyyppi | Office365 |
    | Käyttäjänimi | |
    | Salasana tai Azure Key Vault | Salasana |
    | Salasana | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Data Factory -mallien suorittamisen valmisteleminen

Tässä osassa kuvaillaan asetukset, jotka on suoritettava ennen osapuolen postiosoitteen ja osapuolen sähköisen osoitteen Data Factory -mallien suorittamista.

### <a name="setup-to-run-the-party-postal-address-template"></a>Osapuolen postiosoitemallin suorituksen asetukset

1. Kirjaudu sisään Customer Engagement -sovelluksiin ja siirry kohtaan **Asetukset** \> **Mukautusasetukset**. Määritä sitten järjestelmän järjestelmänvalvojan tilin aikavyöhykeasetus **Yleiset**-välilehdessä. Aikavyöhykkeen on oltava UTC (Coordinated Universal Time) -muodossa, jotta sovellusten postiosoitteen "voimassaolon alkamisaika"- ja "voimassaolon päättymisaika" -päivämäärät päivittyvät rahoitus- ja toiminta -sovelluksista.

    ![Järjestelmän järjestelmänvalvojan tilin aikavyöhykeasetus.](media/ADF-1.png)

2. Luo Data Factoryn **Hallinta**-välilehden **Yleiset parametrit** -kohdassa seuraava yleinen parametri.

    | Numero | Nimi | Tyyppi | Arvo |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | merkkijono | Tämä parametri lisää sarjanumeron juuri luotuihin postiosoitteisiin etuliitteeksi. Varmista, että kirjoitat merkkijonon, joka ei ole ristiriidassa rahoitus- ja toiminta -sovellusten ja Customer Engagement -sovellusten postiosoitteiden kanssa. Käytä esimerkiksi merkkijonoa **ADF-PAD-**. |

    ![Hallinta-välilehdessä luotu yleinen PostalAddressIdPrefix-parametri.](media/ADF-2.png)

3. Kun olet valmis, valitse **Julkaise kaikki**.

    ![Julkaise kaikki -painike.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Osapuolen sähköisen osoitteen mallin suorituksen asetukset

1. Luo Data Factoryn **Hallinta**-välilehden **Yleiset parametrit** -kohdassa seuraavat yleiset parametrit.

    | Numero | Nimi | Tyyppi | Arvo |
    |---|---|---|---|
    | 1 | IsFOSource | bool | Tämä parametri määrittää, mitkä ensisijaiset järjestelmäosoitteet korvataan ristiriitojen yhteydessä. Jos arvo on **true**, rahoitus- ja toiminta -sovellusten ensisijaiset osoitteet korvaavat Customer Engagement -sovellusten ensisijaiset osoitteet. Jos arvo on **false**, customer engagement -sovellusten ensisijaiset osoitteet korvaavat rahoitus- ja toiminta -sovellusten ensisijaiset osoitteet. |
    | 2 | ElectronicAddressIdPrefix | merkkijono | Tämä parametri lisää sarjanumeron juuri luotuihin sähköisiin osoitteisiin etuliitteeksi. Varmista, että kirjoitat merkkijonon, joka ei ole ristiriidassa rahoitus- ja toiminta -sovellusten ja Customer Engagement -sovellusten sähköisten osoitteiden kanssa. Käytä esimerkiksi merkkijonoa **ADF-EAD-**. |

    ![Yleiset IsFOSource- ja ElectronicAddressIdPrefix-parametrit, jotka on luotu Hallinta-välilehdessä.](media/ADF-4.png)

2. Kun olet valmis, valitse **Julkaise kaikki**.

## <a name="run-the-templates"></a>Suorita mallit

1. Lopeta rahoitus- ja toiminta -sovellusta käyttävä seuraava kaksoiskirjoituksen **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-yhdistämismääritys:

    + Asiakkaat V3 (accounts)
    + Asiakkaat V3 (yhteyshenkilöt)
    + CDS-kontaktit V2 (yhteyshenkilöt)
    + CDS-kontaktit V2 (yhteyshenkilöt)
    + Toimittajat V2 (msdyn_vendors)

2. Varmista, että yhdistämismääritykset on poistettu kohteen **msdy_dualwriteruntimeconfig**-taulusta Dataversessa.
3. Asenna [kaksoskirjoituksen osapuoli ja yleisiä osoitekirjaratkaisuja](https://aka.ms/dual-write-gab) AppSourcesta.
4. Jos seuraavat taulut sisältävät tietoja rahoitus- ja toiminta -sovelluksessa, suorita niiden **ensimmäinen synkronointi**:

    + Tervehdykset
    + Henkilökohtaisten luonteenpiirteiden tyypit
    + Loppusanat
    + Yhteyshenkilöiden arvonimet
    + Päätöksentekoroolit
    + Kanta-asiakastasot

5. Poista seuraavat vaiheet käytöstä Customer Engagement -sovelluksessa:

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

    + Customeraddress

        + Luo

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: customeraddress-kohteen luonti

        + Päivitys

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: customeraddress-kohteen päivitys

        + Poista

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: customeraddress-kohteen poisto

    + msdyn_partypostaladdress

        + Luo

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress-kohteen luonti
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress-kohteen luonti

        + Päivitys

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress-kohteen päivitys
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress-kohteen päivitys

    + msdyn_postaladdress

        + Luo

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: msdyn_postaladdress-kohteen luonti
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: msdyn_postaladdress-kohteen luonti
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress-kohteen luonti

        + Päivitys

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: msdyn_postaladdress-kohteen päivitys
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress-kohteen päivitys

    + msdyn_partyelectronicaddress

        + Luo

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress-kohteen luonti

        + Päivitys

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress-kohteen päivitys

        + Poista

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress-kohteen poisto

6. Poista seuraavat vaiheet käytöstä Customer Engagement -sovelluksen työnkuluissa:

    + Toimittajien luonti Tilit-taulussa
    + Toimittajien luonti Tilit-taulussa
    + Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa
    + Luo henkilötyyppisiä toimittajia Toimittajat-taulussa
    + Toimittajien päivitys Tilit-taulussa
    + Toimittajien päivitys Toimittajat-taulussa
    + Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa
    + Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa

7. Suorita malli Data Factoryssä valitsemalla **Käynnistä nyt** seuraavan kuvan mukaisesti. Tämän prosessin suoritus saattaa kestää joitakin tunteja tietojen määrän perusteella.

    ![Suoritetaan mallia.](media/data-factory-trigger.png)

    > [!NOTE]
    > Jos olet muokannut **tiliä**, **yhteyshenkilöä** ja **toimittajaa**, sinun on muokattava mallia.

8. Tuo uudet **osapuoli**-tietueet rahoitus- ja toiminta -sovellukseen.

    1. Lataa **FONewParty.csv**-tiedosto Azure Blob -objektisäilöstä. Polku on **partybootstrapping/output/FONewParty.csv**.
    2. Muunna **FONewParty.csv**-tiedosto Excel-tiedostoksi ja tuo Excel-tiedosto rahoitus- ja toiminta -sovellukseen. Jos CSV-tuonti toimii sinulle, voit tuoda CSV-tiedoston vaihtoehtoisesti suoraan. Tämän vaiheen suoritus saattaa kestää joitakin tunteja tietojen määrän perusteella. Lisätietoja on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../data-import-export-job.md).

    ![Osapuolen Dataverse-tietueiden tuominen.](media/data-factory-import-party.png)

9. Suorita Data Factoryssa osapuolen postiosoitteen ja osapuolen sähköisen osoitteen mallit toisensa perään.

    + Osapuolen postiosoitemalli päivittää ja lisää (upsert) kaikki Customer Engagement -sovelluksen postiosoitetietueet ja liittää ne vastaaviin **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-tietueisiin. Lisäksi se luo kolme .csv-tiedostoa: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv ja ImportFONewPostalAddress.csv.
    + Osapuolen sähköisen osoitteen malli päivittää ja lisää (upsert) kaikki Customer Engagement -sovelluksen sähköisten osoitteiden tietueet ja liittää ne vastaaviin **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-tietueisiin. Se luo myös yhden .csv-tiedoston: ImportFONewElectronicAddress.csv.

    ![Osapuolen postiosoitteen ja osapuolen sähköisen osoitteen mallien suorittaminen.](media/ADF-7.png)

10. Jotta rahoitus- ja toiminta -sovellukseen voidaan päivittää nämä tiedot, sinun on muunnettava .csv-tiedostot Excel-työkirjaksi ja [tuotava se rahoitus- ja toiminta -sovellukseen](/data-entities/data-import-export-job). Jos CSV-tuonti toimii sinulle, voit tuoda CSV-tiedostot vaihtoehtoisesti suoraan. Tämän vaiheen suoritus saattaa kestää joitakin tunteja määrän perusteella.

    ![Onnistunut tuonti.](media/ADF-8.png)

11. Ota seuraavat vaiheet käyttöön Customer Engagement -sovelluksessa:

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

    + msdyn_partypostaladdress

        + Luo

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress-kohteen luonti
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress-kohteen luonti

        + Päivitys

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress-kohteen päivitys
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress-kohteen päivitys

    + msdyn_postaladdress

        + Luo

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: msdyn_postaladdress-kohteen luonti
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: msdyn_postaladdress-kohteen luonti
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress-kohteen luonti

        + Päivitys

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: msdyn_postaladdress-kohteen päivitys
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress-kohteen päivitys
 
    + msdyn_partyelectronicaddress

        + Luo

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress-kohteen luonti

        + Päivitys

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress-kohteen päivitys

        + Poista

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress-kohteen poisto

12. Aktivoi seuraavat työnkulut Customer Engagement -sovelluksessa, jos olet poistanut niiden aktivoinnin aiemmin:

    + Toimittajien luonti Tilit-taulussa
    + Toimittajien luonti Tilit-taulussa
    + Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa
    + Luo henkilötyyppisiä toimittajia Toimittajat-taulussa
    + Toimittajien päivitys Tilit-taulussa
    + Toimittajien päivitys Toimittajat-taulussa
    + Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa
    + Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa

13. Suorita **osapuolen** tietueisiin liittyvät yhdistämismääritykset [osapuolen ja yleisen osoitekirjan](party-gab.md) ohjeiden mukaisesti.

## <a name="explanation-of-the-data-factory-templates"></a>Data Factory -mallien kuvaus

Tässä osassa on tietoja kunkin Data Factory -mallin vaiheista.

### <a name="steps-in-the-party-template"></a>Osapuolimallin vaiheet

1. Vaiheet 1-6 yksilöivät yritykset, jotka on otettu käyttöön kaksoiskirjoitukselle, ja rakentaa niille suodatinlausekkeen.
2. Vaiheet 7-1 – 7-9 hakevat tietoja sekä rahoitus- ja toiminta -sovelluksesta että Customer Engagement -sovelluksesta ja valmistavat tiedot päivitystä varten.
3. Vaiheet 8-9 vertaavat rahoitus- ja toiminta -sovelluksen ja Customer Engagement -sovelluksen välistä **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-tietueiden osapuolinumeroa. Kaikki tietueet, joissa ei ole osapuolen numeroa, ohitetaan.
4. Vaihe 10 luo kaksi .csv-tiedostoa osapuolitietueille, jotka on luotava Customer Engagement -sovelluksessa ja rahoitus- ja toiminta -sovelluksessa.

    - **FOCDSParty.csv** – Tämä tiedosto sisältää molempien järjestelmien kaikki osapuolitietueet riippumatta siitä, onko yritys otettu käyttöön kaksoiskirjoitukselle.
    - **FONewParty.csv** – Tämä tiedosto sisältää osajoukon osapuolitietueita, joista Dataverse on tietoinen (esimerkiksi **Prospekti**-tyypin tilit).

5. Vaihe 11 luo osapuolet Customer Engagement -sovelluksessa.
6. Vaihe 12 hakee osapuolten yleiset yksilölliset tunnukset (GUID) Customer Engagement -sovelluksesta ja määrittää ne vaiheittain siten, että ne voidaan liittää **tili**-, **yhteyshenkilö**- ja **toimittaja**-tietueisiin seuraavissa vaiheissa.
7. Vaihe 13 liittää **tilin**, **yhteyshenkilön** ja **toimittajan** tietueet osapuolen GUID-tunnuksiin.
8. Vaiheet 14-1 – 14-3 päivittävät Customer Engagement -sovelluksen **tili**-, **yhteyshenkilö**- ja **toimittaja**-tietueisiin osapuolen GUID-tunnuksen.
9. Vaiheet 15-1 – 15-3 valmistelevat **Osapuolen yhteyshenkilö** -tietueet **tili**-, **yhteyshenkilö**- ja **toimittaja**-tietueita varten.
10. Vaiheet 16-1 – 16-7 hakevat viitetietoja, kuten tervehdyksiä ja henkilökohtaisia luonnetyyppejä, ja liittävät ne **Osapuolen yhteyshenkilö** -tietueisiin.
11. Vaihe 17 yhdistää **Osapuolen yhteyshenkilö** -tietueet **tili**-, **yhteyshenkilö**- ja **toimittaja**-tietueisiin.
12. Vaihe 18 tuo **Osapuolen yhteyshenkilö** -tietueet Customer Engagement -sovellukseen.

### <a name="steps-in-the-party-postal-address-template"></a>Osapuolen postiosoitemallin vaiheet

1. Vaiheet 1-1 – 1-10 hakevat tietoja sekä rahoitus- ja toiminta -sovelluksesta että Customer Engagement -sovelluksesta ja valmistavat tiedot päivitystä varten.
2. Vaihe 2 denormalisoi rahoitus- ja toiminta -sovelluksen postiosoitetiedot liittämällä postiosoitteen ja osapuolen postiosoitteen.
3. Vaihe 3 poistaa kaksoisarvot ja yhdistää Customer Engagement -sovelluksen tili-, yhteyshenkilö- ja toimittajaosoitetiedot.
4. Vaihe 4 luo rahoitus- ja toiminta -sovellukselle .csv-tiedostot, jotka luovat uusia osoitetietoja, jotka perustuvat tili-, yhteyshenkilö- ja toimittajaosoitteisiin.
5. Vaihe 5-1 luo .csv-tiedostot Customer Engagement -sovellukselle kaikkien osoitetietojen luomiseen sekä rahoitus- ja toiminta -sovelluksen että Customer Engagement -sovelluksen perusteella.
6. Vaihe 5-2 muuntaa .csv-tiedostot manuaalisen tuonnin rahoitus- ja toiminta -tuontimuodoksi.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. Vaihe 6 tuo postiosoitteen keräystiedot Customer Engagement -sovellukseen.
8. Vaihe 7 noutaa postiosoitteen keräystiedot Customer Engagement -sovelluksesta.
9. Vaihe 8 luo asiakkaan osoitetiedot ja liittää postiosoitteen keräystunnuksen.
10. Vaiheet 9-1 – 9-2 yhdistävät osapuolen ja postinumeron keräystunnukset postiosoitteisiin ja osapuolen postiosoitteisiin.
11. Vaiheet 10-1 – 10-3 tuovat asiakkaiden osoitteet, postiosoitteet ja osapuolen postiosoitteet Customer Engagement -sovellukseen.

### <a name="steps-in-the-party-electronic-address-template"></a>Osapuolen sähköisen osoitteen mallin vaiheet

1. Vaiheet 1-1 – 1-5 hakevat tietoja sekä rahoitus- ja toiminta -sovelluksesta että Customer Engagement -sovelluksesta ja valmistavat tiedot päivitystä varten.
2. Vaihe 2 konsolidoi sähköiset osoitteet Customer Engagement -sovelluksessa tili-, yhteyshenkilö- ja toimittajayksiköistä.
3. Vaihe 3 yhdistää ensisijaiset sähköiset osoitetiedot Customer Engagement -sovelluksesta ja rahoitus- ja toiminta -sovelluksesta.
4. Vaihe 4 luo .csv-tiedostot.

    - Luo rahoitus- ja toiminta -sovellukselle uudet sähköiset osoitetiedot tilin, yhteyshenkilön ja toimittajan osoitteiden perusteella.
    - Luo uusia sähköisiä osoitetietoja Customer Engagement -sovellusta varten. Tiedot perustuvat rahoitus- ja toiminta -sovelluksen sähköisiin osoitteisiin sekä tili-, yhteyshenkilö- ja toimittajaosoitteisiin.

5. Vaihe 5-1 tuo sähköiset osoitteet Customer Engagement -sovellukseen.
6. Vaihe 5-2 luo .csv-tiedostoja päivittämään asiakkaiden ja yhteyshenkilöiden ensisijaiset osoitteet Customer Engagement -sovelluksessa.
7. Vaiheet 6-1 – 6-2 tuovat tilien ja yhteyshenkilöiden ensisijaiset osoitteet Customer Engagement -sovellukseen.

## <a name="troubleshooting"></a>Vianmääritys

1. Jos prosessi epäonnistuu, suorita Data Factory uudelleen. Aloita epäonnistuneesta tehtävästä.
2. Osa tiedostoista luodaan data factoryssa, jota voit käyttää tietojen oikeellisuustarkistusta varten.
3. Data factory suoritetaan csv-tiedostojen perusteella. Jos siis kenttäarvossa on pilkku, se voi vaikuttaa tuloksiin. Kaikki pilkut on poistettava kenttäarvoista.
4. **Seuranta**-välilehdessä on tietoja kaikista vaiheista ja käsitellyistä tiedoista. Valitse tietty virheenkorjausvaihe.

    ![Seuranta-välilehti.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Lisätietoja mallista

Lisätietoja mallista: [Azure Data Factory -mallin lueminut-tiedoston kommentit](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
