---
title: Ongelmien vianmääritys synkronoinnin aikana
description: Tässä artikkelissa on vianmääritys tietoja, joiden avulla voit korjata, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.
author: RamaKrishnamoorthy
ms.date: 06/24/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d9d74eea90cc2dfca2d5decf6e5cd1d7f52da2a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289481"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Ongelmien vianmääritys synkronoinnin aikana

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa on vianmääritystietoja kaksoiskirjoituksen integroinnista talous- ja toimintosovellusten sekä Dataversen välillä. Erityisesti se tarjoaa tietoa, joiden avulla voit korjata virheitä, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.

> [!IMPORTANT]
> Jotkin tämän artikkelin osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoft Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Tarkista ensimmäisen synkronoinnin virheet talous- ja toimintosovelluksessa

Kun otat yhdistämismallit käyttöön, karttojen tilan on oltava **Käytössä**. Jos tila on **ei käynnissä**, alkuperäisen synkronoinnin aikana ilmeni virheitä. Voit tarkastella virheitä valitsemalla **kaksoiskirjoitus**-sivun **ensimmäiset synkronointitiedot**-välilehden.

![Virhe Alkuperäisen synkronoinnin tiedot -välilehdessä.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Alkuperäistä synkronointia ei voi suorittaa loppuun: 400 virheellinen pyyntö

**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität suorittaa yhdistämismääritystä ja alkuperäistä synkronointia:

*(\[Virheellinen pyyntö\], etäpalvelin palautti virheen: (400) Virheellinen pyyntö.), AX-vienti havaitsi virheen.*

Esimerkki täydestä virheviestistä.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Jos tämä virhe ilmenee jatkuvasti etkä voi suorittaa alkuperäistä synkronointia loppuun, korjaa ongelma noudattamalla seuraavia ohjeita.

1. Kirjaudu sisään talous- ja toimintosovelluksen näennäiskoneeseen (VM).
2. Avaa Microsoft Management Console.
3. Varmista **Palvelut**-ruudussa, että Microsoft Dynamics 365 -tietojen tuonnin vientikehyspalvelu on käytössä. Käynnistä se uudelleen, jos se on pysäytetty, koska ensimmäinen synkronointi edellyttää sitä.

## <a name="initial-synchronization-error-403-forbidden"></a>Ensimmäinen synkronointivirhe: 403 kielletty

Seuraava virhesanoma saattaa tulla näyttöön alkuperäisen synkronoinnin aikana:

*(\[Kielletty\], Etäpalvelin palautti virheen: (403) Kielletty.), AX-vienti kohtasi virheen*

Korjaa ongelma seuraavien ohjeiden mukaisesti.

1. Kirjaudu talous- ja toimintosovellukseen.
2. Poista **Azure Active Directory -sovellukset** -sivulla **DtAppID**-asiakasohjelma ja lisää se sitten uudelleen.

![DtAppID-asiakasohjelma Azure AD -sovellusten luettelossa.](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Itseensä viittaus- tai kehäviittausvirheet ensimmäisen synkronoinnin aikana

Näyttöön saattaa tulla virhesanoma, jos jollakin yhdistämismäärityksistä on omia viittauksia tai kehäviittauksia. Virheet kuuluvat seuraaviin luokkiin:

- [Virheet Toimittajat V2 msdyn_vendors -taulun yhdistämismäärityksessä](#error-vendor-map)
- [Virheet Asiakkaat V3 tileille -taulun yhdistämismäärityksessä](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Toimittajat V2 msdyn_vendors -taulun yhdistämismäärityksen virheiden ratkaiseminen

**Toimittajat V2** kohteeseen tapahtuvassa **msdyn\_vendors** yhdistämismäärityksessä voi esiintyä ensimmäisen synkronoinnin virheitä, jos tauluissa on aiemmin luotuja rivejä, joiden **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-sarakkeissa on arvo. Nämä virheet johtuvat siitä, että **InvoiceVendorAccountNumber** on itseviittaava sarake ja **PrimaryContactPersonId** on kehäviittaus toimittajan yhdistämismäärityksessä.

Näiden virhesanomien muoto on seuraavanlainen:

*Kentän GUID-arvon selvittäminen ei onnistunut: \<field\>. Hakua ei löydy: \<value\>. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Seuraavassa on muutamia esimerkkejä:

- *Kentän GUID-arvon selvittäminen ei onnistunut: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Hakua ei löydy: 000056. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Kentän GUID-arvon selvittäminen ei onnistunut: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Hakua ei löydy:V24-1 . Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Jos toimittajataulun rivien **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-sarakkeissa on arvoja, suorita ensimmäinen synkronointi loppuun seuraavien ohjeiden mukaisesti:

1. Poista talous- ja toimintosovelluksessa **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-sarakkeet yhdistämismäärityksestä ja tallenna sitten yhdistämismääritys.

    1. Valitse **Toimittajat V2 (msdyn\_vendors)** -kaksoiskirjoituksen määrityssivun **Taulujen yhdistämismääritykset** -välilehden vasemmassa suodattimessa **Talous- ja toimintosovellukset.Toimittajat V2**. Valitse oikeanpuoleisesta suodattimesta **Sales.Vendor**.
    2. Käytä hakusanaa **primarycontactperson** ja etsi **PrimaryContactPersonId**-lähdesarake.
    3. Valitse ensin **Toiminnot** ja sitten **Poista**.

        ![PrimaryContactPersonId-sarakkeen poistaminen.](media/vend_selfref3.png)

    4. Poista **InvoiceVendorAccountNumber**-sarake samalla tavalla.

        ![InvoiceVendorAccountNumber-sarakkeen poistaminen.](media/vend-selfref4.png)

    5. Tallenna yhdistämismäärityksen muutokset.

2. Poista **Toimittajien V2** -taulun muutosten seuranta käytöstä.

    1. Valitse **Tiedonhallinta**-työtilassa **Tietotaulut**-ruutu.
    2. Valitse **Toimittajat V2**-taulu.
    3. Valitse toimintoruudussa **Vaihtoehdot** ja valitse sitten **Muutosten seuranta**.

        ![Muutosten seuranta -vaihtoehdon valitseminen.](media/selfref_options.png)

    4. Valitse **Poista muutosten seuranta käytöstä**.

        ![Muutosten seurannan käytöstä poistamisen valinta.](media/selfref_tracking.png)

3. Suorita **Toimittajat V2 (msdyn\_vendors)** -yhdistämismäärityksen ensimmäinen synkronointi. Ensimmäisen synkronoinnin pitäisi onnistua ilman virheitä.
4. Suorita **CDS-yhteyshenkilöt V2 (yhteyshenkilöt)** -yhdistämismäärityksen ensimmäinen synkronointi. Tämä yhdistämismääritys on synkronoitava, jos haluat synkronoida toimittajataulun ensisijaisen yhteyshenkilösarakkeen, koska ensimmäinen synkronointi on tehtävä myös yhteyshenkilörivien osalta.
5. Lisää **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-sarakkeet takaisin **Toimittajat V2 (msdyn\_vendors)** -yhdistämismääritykseen ja tallenna yhdistämismääritys sitten.
6. Suorita **Toimittajat V2 (msdyn\_vendors)** -yhdistämismäärityksen ensimmäinen synkronointi uudelleen. Koska muutosten seuranta on poistettu käytöstä, kaikki taulut synkronoidaan.
7. Ota **Toimittajien V2** -taulun muutosten seuranta takaisin käyttöön.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Asiakkaat V3 tileille -taulun yhdistämismäärityksen virheiden ratkaiseminen

**Asiakkaat V3** **tileille** -yhdistämismäärityksessä voi esiintyä ensimmäisen synkronoinnin virheitä, jos tauluissa on aiemmin luotuja rivejä, joiden **ContactPersonID**- ja **InvoiceAccount**-sarakkeissa on arvo. Näiden virheiden syynä on se, että **InvoiceAccount** on itseviittaava sarake ja **ContactPersonID** on kehäviittaus toimittajan yhdistämismäärityksessä.

Näiden virhesanomien muoto on seuraavanlainen:

*Kentän GUID-arvon selvittäminen ei onnistunut: \<field\>. Hakua ei löydy: \<value\>. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Seuraavassa on muutamia esimerkkejä:

- *Kentän GUID-arvon selvittäminen ei onnistunut: primarycontactid.msdyn\_contactpersonid. Hakua ei löydy: 000056. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Kentän GUID-arvon selvittäminen ei onnistunut: msdyn\_billingaccount.accountnumber. Hakua ei löydy: 1206-1. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Jos asiakastaulun rivien **ContactPersonID**- ja **InvoiceAccount**-sarakkeissa on arvoja, suorita ensimmäinen synkronointi loppuun seuraavien ohjeiden mukaisesti: Tämän menetelmän avulla voit käyttää kaikkia valmiita tauluja, kuten **Tilejä** ja **Yhteyshenkilöitä**.

1. Poista talous- ja toimintosovelluksessa **ContactPersonID**- ja **InvoiceAccount** -sarakkeissa **Asiakkaat V3 (tilit)** -yhdistämismäärityksestä ja tallenna sitten yhdistämismääritys.

    1. Valitse **Asiakkaat V3 (tilit)** -kaksoiskirjoituksen määrityssivun **Taulujen yhdistämismääritykset** -välilehden vasemmassa suodattimessa **Talous- ja toimintosovellus.Asiakkaat V3**. Valitse oikeanpuoleisesta suodattimesta **Dataverse.Account**.
    2. Käytä hakusanaa **contactperson** ja etsi **ContactPersonID** lähdesarake.
    3. Valitse ensin **Toiminnot** ja sitten **Poista**.

        ![ContactPersonID-sarakkeen poistaminen.](media/cust_selfref3.png)

    4. Poista **InvoiceAccount**-sarake samalla tavalla.

        ![InvoiceAccount-sarakkeen poistaminen.](media/cust_selfref4.png)

    5. Tallenna yhdistämismäärityksen muutokset.

2. Poista **Toimittajien V3** -taulun muutosten seuranta käytöstä.

    1. Valitse **Tiedonhallinta**-työtilassa **Tietotaulut**-ruutu.
    2. Valitse **Asiakkaat V3** -taulu.
    3. Valitse toimintoruudussa **Vaihtoehdot** ja valitse sitten **Muutosten seuranta**.

        ![Muutosten seuranta -vaihtoehdon valitseminen.](media/selfref_options.png)

    4. Valitse **Poista muutosten seuranta käytöstä**.

        ![Muutosten seurannan käytöstä poistamisen valinta.](media/selfref_tracking.png)

3. Suorita **Asiakkaat V3 (tilit)** -yhdistämismäärityksen ensimmäinen synkronointi. Ensimmäisen synkronoinnin pitäisi onnistua ilman virheitä.
4. Suorita **CDS-yhteyshenkilöt V2 (yhteyshenkilöt)** -yhdistämismäärityksen ensimmäinen synkronointi.

    > [!NOTE]
    > Kahdella yhdistämismäärityksellä on sama nimi. Varmista, että valitse yhdistämismäärityksen, jonka **Tiedot**-välilehdessä on seuraava kuvaus: **Kaksoiskirjoitusmalli synkronointiin FO.CDS Toimittajayhteyshenkilöiden V2 ja CDS.Contacts välillä. Tarvitaan uusi paketti \[Dynamics365SupplyChainExtended\].**

5. Lisää **InvoiceAccount**- ja **ContactPersonId** -sarakkeet takaisin **Asiakkaat V3 (tilit)** -yhdistämismääritykseen ja tallenna sitten yhdistämismääritys. Sekä **InvoiceAccount**- että **ContactPersonId**-sarakkeet ovat nyt taas synkronoinnin live-tilan osa. Seuraavassa vaiheessa tehdään näiden sarakkeiden ensimmäinen synkronointi.
6. Suorita uudelleen **Asiakkaat V3 (tilit)** -yhdistämismäärityksen ensimmäinen synkronointi. Koska muutosten seuranta on poistettu käytöstä, **InvoiceAccount**- ja **ContactPersonId** -tiedot synkronoidaan talous- ja toimintosovelluksesta Dataverseen.
7. **InvoiceAccount**- ja **ContactPersonId** -tietojen synkronoinnissa Dataversesta talous- ja toimintosovellukseen on käytettävä tietojen integrointiprojektia.

    1. Luo Power Appsissa tietojen integrointiprojekti **Sales.Account**- ja **Talous- ja toimintosovellukset.Asiakkaat V3** -taulujen välille. Tietojen suunnan on oltava Dataversestä talous- ja toimintosovellukseen. Koska **InvoiceAccount** on uusi kaksoiskirjoituksen määrite, sen ensimmäinen synkronointi kannattaa ehkä ohittaa. Lisätietoja on kohdassa [Tietojen integrointi Dataverse -ratkaisuun](/power-platform/admin/data-integrator).

        Seuraavassa kuvassa on projekti, joka päivittää **CustomerAccount**- ja **ContactPersonId**-määritteet.

        ![CustomerAccount- ja ContactPersonId-määritteet päivittävä tietojen integrointiprojekti.](media/cust_selfref6.png)

    2. Lisää yrityksen ehdot suodattimen Dataversen puolelle, jotta vain suodatusehtoja vastaavat rivit päivitetään talous- ja toimintosovelluksessa. Lisää suodatin valitsemalla suodatinpainike. Voit sitten lisätä **Muokkaa kyselytä** -valintaikkunassa suodatinkyselyn, kuten **\_msdyn\_company\_value eq '\<guid\>'**.

        > [HUOMAUTUS] Jos suodatinpainike ei ole näkyvissä, luo tukipyyntö, jotta tietojen integrointiryhmä voi ottaa suodattimen käyttöön vuokraajassa.

        Jos suodatinkyselyä **\_msdyn\_company\_value** ei määritetä, kaikki rivit synkronoidaan.

        ![Suodatinkyselyn lisääminen.](media/cust_selfref7.png)

    Rivien ensimmäinen synkronointi on nyt valmis.

8. Ota muutosten seuranta taas käyttöön talous- ja toimintosovelluksen **Asiakkaat V3** -taulussa.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>Ensimmäisen synkronoinnin virheet, kun yhdistämisissä on yli 10 hakukenttää.

Seuraava sanoma voidaan antaa, kun yritetään suorittaa ensimmäinen synkronointi ja virheitä on **Asiakkaat V3 tileille**, **Myyntitilaukset** yhdistämismäärityksissä tai missä tahansa yhdistämisessä, jossa on yi 10 hakukenttää.

*CRMExport: Paketti suoritettu. Virheen kuvaus 5 yritystä hakea tietoja osoitteesta https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$orderby=accountnumber asc epäonnistui.*

Kyselyn hakurajoituksen vuoksi ensimmäinen synkronointi epäonnistuu, entiteetin yhdistämismäärityksessä on yli 10 hakua. Lisätietoja on kohdassa [Liittyvän taulukon tietueiden noutaminen kyselyn avulla](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

Ongelma korjataan seuraavasti:

1. Poista valinnaisia hakukenttiä kaksoiskirjoituksen entiteetin yhdistämismäärityksestä siten, että hakujen määrä on enintään 10.
2. Tallenna määritys ja tee ensimmäinen synkronointi.
3. Kun ensimmäisen vaiheen ensimmäinen synkronointi onnistuu, lisää loput hakukentät ja poista hakukentät, jotka synkronoitiin ensimmäisessä vaiheessa. Varmista, että hakukenttien määrä on enintään 10. Tallenna määritys ja suorita ensimmäinen synkronointi.
4. Toista nämä vaiheet, kunnes kaikki hakukentät on synkronoitu.
5. Lisää kaikki hakukentät takaisin yhdistämismääritykseen, tallenna määritys ja suorita yhdistämismääritys **Ohita ensimmäinen synkronointi** valittuna.

Tämä prosessi antaa mahdollisuuden yhdistämismääritystä live-synkronointitilassa.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>Osapuolen postiosoitteen ja osapuolen sähköisten osoitteiden ensimmäisen synkronoinnin tunnettu ongelma

Seuraava virhesanoma voi avautua kun osapuolen postiosoitteen ja osapuolen sähköisten osoitteiden ensimmäinen synkronointi yritetään suorittaa:

*Osapuolen numeroa ei löytynyt Dataversesta.*

Tämä alue määritetään talous- ja toimintosovellusten **DirPartyCDSEntity**-kohdassa suodattamaan **Henkilö**- ja **Organisaatio**-tyypin osapuolia. Tämän vuoksi **CDS-osapuolet – msdyn_parties** -yhdistämismäärityksen ensimmäinen synkronointi ei synkronoi muita osapuolityyppejä, kuten **Yritys** ja **Toimintayksikkö**. Virhe voi esiintyä, kun ensimmäistä **CDS-osapuolen postiosoitteet (msdyn_partypostaladdresses)**- tai **Osapuolen yhteyshenkilöt V3 (msdyn_partyelectronicaddresses)** -synkronointia.

Korjausta, jolla osapuolityyppialue voidaan poistaa talous- ja toimintosovellusentiteetistä, kehitetään, jotta kaiken tyyppisten osapuolien synkronointi Dataverseen onnistuu.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Esiintyykö asiakas- tai yhteyshenkilötietojen ensimmäisessä synkronoinnissa suorituskykyongelmia?

Jos **Asiakas**-tietojen ensimmäinen synkronointi on suoritettu ja **Asiakas**-yhdistämismäärityksiä suoritetaan, minkä jälkeen suoritetaan **Yhteyshenkilöt**-tietojen ensimmäisen synkronointi, **Yhteyshenkilöt**-osoitteiden **LogisticsPostalAddress**- ja **LogisticsElectronicAddress**-taulukkoja koskevien lisäysten ja päivitysten aikana voi esiintyä suorituskykyongelmia. Samaa yleistä postiosoitteen ja sähköisen osoitteen taulukoita seurataan **CustCustomerV3Entity**- ja **VendVendorV2Entity**-entiteettien osalta, minkä lisäksi kaksoiskirjoitus yrittää muodostaa lisää kyselyjä kirjoittamaan tietoja toiselle puolelle. Jos ensimmäinen **Asiakas**-synkronointi on jo suoritettu, pysäytä vastaava yhdistämismääritys **Yhteyshenkilöt**-tietojen ensimmäisen synkronoinnin ajaksi. Tee samoin **Toimittaja**-tietojen kohdalla. Kun ensimmäinen synkronointi on valmis, kaikki yhdistämismääritykset voidaan sitten suorittaa ohittamalla ensimmäinen synkronointi.

## <a name="float-data-type-that-has-a-zero-value-cant-be-synchronized"></a>Liukuluku-tietotyyppiä, jolla on nolla-arvo, ei voi synkronoida

Ensimmäinen synkronointi voi epäonnistua niiden tietueiden osalta, joiden hintakentässä on nolla-arvo. Tällaisia kenttiä ovat esimerkiksi **Kiinteä maksun summa** tai **Summa** tapahtumavaluuttana. Tässä tapauksessa tuloksena seuraavaa esimerkkiä muistuttava virhesanoma:

*Syöteparametreja tarkistettaessa tapahtui virhe: Microsoft.OData.ODataException: literaalia 000000 ei voi muuntaa odotetuksi arvoksi type'Edm.Decimal',...*

Ongelma liittyy **Kielen aluekohtainen asetus** -arvoon **Tietojen hallinta** -moduulin **Lähdetietojen muodot** -kohdassa. Vaihda **Kielen aluekohtainen asetus** -kentän arvoksi **en-us** ja yritä sitten uudelleen.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

