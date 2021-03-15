---
title: Ongelmien vianmääritys synkronoinnin aikana
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a2f0e0cbf0f8710dc020a48506775fa28df9c2d2
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744634"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Ongelmien vianmääritys synkronoinnin aikana

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä. Erityisesti se tarjoaa tietoa, joiden avulla voit korjata virheitä, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Finance and Operations -sovelluksen ensimmäisten synkronointivirheiden tarkistaminen

Kun otat yhdistämismallit käyttöön, karttojen tilan on oltava **Käytössä**. Jos tila on **ei käynnissä**, alkuperäisen synkronoinnin aikana ilmeni virheitä. Voit tarkastella virheitä valitsemalla **kaksoiskirjoitus**-sivun **ensimmäiset synkronointitiedot**-välilehden.

![Virhe Alkuperäisen synkronoinnin tiedot -välilehdessä](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Alkuperäistä synkronointia ei voi suorittaa loppuun: 400 virheellinen pyyntö

**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität suorittaa yhdistämismääritystä ja alkuperäistä synkronointia:

*(\[Virheellinen pyyntö\], Etäpalvelin palautti virheen: (400) Virheellinen pyyntö.), AX-vienti kohtasi virheen*

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

1. Kirjaudu sisään virtuaalikone (VM) Finance and Operationsille -sovellukseen.
2. Avaa Microsoft Management Console.
3. Varmista **Palvelut**-ruudussa, että Microsoft Dynamics 365 -tietojen tuonnin vientikehyspalvelu on käytössä. Käynnistä se uudelleen, jos se on pysäytetty, koska ensimmäinen synkronointi edellyttää sitä.

## <a name="initial-synchronization-error-403-forbidden"></a>Ensimmäinen synkronointivirhe: 403 kielletty

Seuraava virhesanoma saattaa tulla näyttöön alkuperäisen synkronoinnin aikana:

*(\[Kielletty\], Etäpalvelin palautti virheen: (403) Kielletty.), AX-vienti kohtasi virheen*

Korjaa ongelma seuraavien ohjeiden mukaisesti.

1. Kirjautuminen Finance and Operations -sovellukseen.
2. Poista **Azure Active Directory -sovellukset** -sivulla **DtAppID**-asiakasohjelma ja lisää se sitten uudelleen.

![DtAppID-asiakasohjelma Azure AD -sovellusten luettelossa](media/aad_applications.png)

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

1. Poista Finance and Operations -sovelluksessa **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-sarakkeet yhdistämismäärityksestä ja tallenna sitten yhdistämismääritys.

    1. Valitse **Toimittajat V2 (msdyn\_vendors)** -kaksoiskirjoituksen määrityssivun **Taulujen yhdistämismääritykset** -välilehden vasemmassa suodattimessa **Finance and Operations -sovellukset Toimittajat V2**. Valitse oikeanpuoleisesta suodattimesta **Sales.Vendor**.
    2. Käytä hakusanaa **primarycontactperson** ja etsi **PrimaryContactPersonId**-lähdesarake.
    3. Valitse ensin **Toiminnot** ja sitten **Poista**.

        ![PrimaryContactPersonId-sarakkeen poistaminen](media/vend_selfref3.png)

    4. Poista **InvoiceVendorAccountNumber**-sarake samalla tavalla.

        ![InvoiceVendorAccountNumber-sarakkeen poistaminen](media/vend-selfref4.png)

    5. Tallenna yhdistämismäärityksen muutokset.

2. Poista **Toimittajien V2** -taulun muutosten seuranta käytöstä.

    1. Valitse **Tiedonhallinta**-työtilassa **Tietotaulut**-ruutu.
    2. Valitse **Toimittajat V2**-taulu.
    3. Valitse toimintoruudussa **Vaihtoehdot** ja valitse sitten **Muutosten seuranta**.

        ![Muutosten seuranta -vaihtoehdon valitseminen](media/selfref_options.png)

    4. Valitse **Poista muutosten seuranta käytöstä**.

        ![Muutosten seurannan käytöstä poistamisen valinta](media/selfref_tracking.png)

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

1. Poista Finance and Operations -sovelluksessa **ContactPersonID**- ja **InvoiceAccount** -sarakkeissa **Asiakkaat V3 (tilit)** -yhdistämismäärityksestä ja tallenna sitten yhdistämismääritys.

    1. Valitse **Asiakkaat V3 (tilit)** -kaksoiskirjoituksen määrityssivun **Taulujen yhdistämismääritykset** -välilehden vasemmassa suodattimessa **Finance and Operations -sovellukset. Asiakkaat V3**. Valitse oikeanpuoleisesta suodattimesta **Dataverse.Account**.
    2. Käytä hakusanaa **contactperson** ja etsi **ContactPersonID** lähdesarake.
    3. Valitse ensin **Toiminnot** ja sitten **Poista**.

        ![ContactPersonID-sarakkeen poistaminen](media/cust_selfref3.png)

    4. Poista **InvoiceAccount**-sarake samalla tavalla.

        ![InvoiceAccount-sarakkeen poistaminen](media/cust_selfref4.png)

    5. Tallenna yhdistämismäärityksen muutokset.

2. Poista **Toimittajien V3** -taulun muutosten seuranta käytöstä.

    1. Valitse **Tiedonhallinta**-työtilassa **Tietotaulut**-ruutu.
    2. Valitse **Asiakkaat V3** -taulu.
    3. Valitse toimintoruudussa **Vaihtoehdot** ja valitse sitten **Muutosten seuranta**.

        ![Muutosten seuranta -vaihtoehdon valitseminen](media/selfref_options.png)

    4. Valitse **Poista muutosten seuranta käytöstä**.

        ![Muutosten seurannan käytöstä poistamisen valinta](media/selfref_tracking.png)

3. Suorita **Asiakkaat V3 (tilit)** -yhdistämismäärityksen ensimmäinen synkronointi. Ensimmäisen synkronoinnin pitäisi onnistua ilman virheitä.
4. Suorita **CDS-yhteyshenkilöt V2 (yhteyshenkilöt)** -yhdistämismäärityksen ensimmäinen synkronointi.

    > [!NOTE]
    > Kahdella yhdistämismäärityksellä on sama nimi. Varmista, että valitse yhdistämismäärityksen, jonka **Tiedot**-välilehdessä on seuraava kuvaus: **Kaksoiskirjoitusmalli synkronointiin FO.CDS Toimittajayhteyshenkilöiden V2 ja CDS.Contacts välillä. Tarvitaan uusi paketti \[Dynamics365SupplyChainExtended\].**

5. Lisää **InvoiceAccount**- ja **ContactPersonId** -sarakkeet takaisin **Asiakkaat V3 (tilit)** -yhdistämismääritykseen ja tallenna sitten yhdistämismääritys. Sekä **InvoiceAccount**- että **ContactPersonId**-sarakkeet ovat nyt taas synkronoinnin live-tilan osa. Seuraavassa vaiheessa tehdään näiden sarakkeiden ensimmäinen synkronointi.
6. Suorita uudelleen **Asiakkaat V3 (tilit)** -yhdistämismäärityksen ensimmäinen synkronointi. Koska muutosten seuranta on poistettu käytöstä, **InvoiceAccount**- ja **ContactPersonId** -tiedot synkronoidaan Finance and Operations -sovelluksesta Dataverse en.
7. **InvoiceAccount**- ja **ContactPersonId** -tietojen synkronoinnissa Dataversesta Finance and Operations -sovelluksiin on käytettävä tietojen integrointiprojektia.

    1. Luo Power Appsissa tietojen integrointiprojekti **Sales.Account**- ja **Finance and Operations apps.Customers V3** -taulujen välille. Tietojen suunnan on oltava peräisin Dataversestä Finance and Operations -sovellukseen. Koska **InvoiceAccount** on uusi kaksoiskirjoituksen määrite, sen ensimmäinen synkronointi kannattaa ehkä ohittaa. Lisätietoja on kohdassa [Tietojen integrointi Dataverse -ratkaisuun](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Seuraavassa kuvassa on projekti, joka päivittää **CustomerAccount**- ja **ContactPersonId**-määritteet.

        ![CustomerAccount- ja ContactPersonId-määritteet päivittävä tietojen integrointiprojekti](media/cust_selfref6.png)

    2. Lisää yrityksen ehdot suodattimen Dataversen puolelle, jotta vain suodatusehtoja vastaavat rivit päivitetään Finance and Operations -sovelluksessa. Lisää suodatin valitsemalla suodatinpainike. Voit sitten lisätä **Muokkaa kyselytä** -valintaikkunassa suodatinkyselyn, kuten **\_msdyn\_company\_value eq '\<guid\>'**. 

        > [HUOMAUTUS] Jos suodatinpainike ei ole näkyvissä, luo tukipyyntö, jotta tietojen integrointiryhmä voi ottaa suodattimen käyttöön vuokraajassa.

        Jos suodatinkyselyä **\_msdyn\_company\_value** ei määritetä, kaikki rivit synkronoidaan.

        ![Suodatinkyselyn lisääminen](media/cust_selfref7.png)

    Rivien ensimmäinen synkronointi on nyt valmis.

8. Ota muutosten seuranta taas käyttöön Finance and Operations -sovelluksen **Asiakkaat V3** -taulussa.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]