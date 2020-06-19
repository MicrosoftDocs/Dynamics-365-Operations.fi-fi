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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410078"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Ongelmien vianmääritys synkronoinnin aikana

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä. Erityisesti se tarjoaa tietoa, joiden avulla voit korjata virheitä, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Finance and Operations -sovelluksen ensimmäisten synkronointivirheiden tarkistaminen

Kun otat yhdistämismallit käyttöön, karttojen tilan on oltava **Käytössä**. Jos tila on **ei käynnissä**, alkuperäisen synkronoinnin aikana ilmeni virheitä. Voit tarkastella virheitä valitsemalla **kaksoiskirjoitus**-sivun **ensimmäiset synkronointitiedot**-välilehden.

![Alkuperäisen synkronoinnin tiedot -välilehti](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Alkuperäistä synkronointia ei voi suorittaa loppuun: 400 virheellinen pyyntö

**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität suorittaa yhdistämismääritystä ja alkuperäistä synkronointia:

*Etäpalvelin palautti virheen: (400) Virheellinen pyyntö.), AX-vienti kohtasi virheen*

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

![Azure AD -sovellusluettelo](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Itseensä viittaus- tai kehäviittausvirheet alkuperäisen synkronoinnin aikana

Näyttöön saattaa tulla virhesanoma, jos jollakin yhdistämismäärityksistä on omia viittauksia tai kehäviittauksia. Virheet kuuluvat seuraaviin luokkiin:

- [Toimittajat V2 – msdyn_vendors yksikön yhdistämismääritys](#error-vendor-map)
- [Asiakkaat V3 tilien yksikkökartoitukseen](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Ratkaise Toimittajien V2 virhe msdyn_vendors yksikön yhdistämismääritystä varten

Saatat joutua käyttämään seuraavia alkusynkronointivirheitä **Toimittajat V2** - **msdyn_vendors** kartoitukseen, jos entiteeteillä on aiemmin luotuja, **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber** -kenttien arvoja. Tämä johtuu siitä, että **InvoiceVendorAccountNumber** on itseviittaava kenttä ja **PrimaryContactPersonId** on kehäviittaus toimittajan yhdistämismäärityksessä.

*Kentän GUID-arvon selvittäminen ei onnistunut: <field>. Hakua ei löydy: <value>. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

Seuraavassa on muutamia esimerkkejä:

- *Kentän GUID-arvon selvittäminen ei onnistunut: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Hakua ei löydy: 000056. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Kentän GUID-arvon selvittäminen ei onnistunut: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Hakua ei löydy: V24-1. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Jos toimittajakohteen kentissä on arvoja, joiden arvot ovat samat, suorita ensimmäinen synkronointi onnistuneesti noudattamalla alla olevan kohdan ohjeita.

1. Poista Finance and Operations sovelluksessa **PrimaryContactPersonId**- ja **InvoiceVendorAccountNumber**-kentät määrityksestä ja tallenna muutokset.

    1. Siirry toimittajat-version **Toimittajat V2 (msdyn_vendors)** -kaksoiskirjoitusmääritysten sivulle ja valitse **yksiköiden yhdistämismääritykset** -välilehti. Valitse vasemmanpuoleisesta suodattimesta **Finance and Operations -sovellukset. Toimittajat V2**. Valitse oikeanpuoleisesta suodattimesta **Sales.Vendor**.

    2. Katso **primarycontactperson** ja etsi lähdekenttä **PrimaryContactPersonId**.
    
    3. Napsauta **Toiminnot**-painiketta ja valitse **Poista**.
    
        ![Itsenäinen tai kehäviittaus 3](media/vend_selfref3.png)
    
    4. Poista uudelleen, jos haluat poistaa **InvoiceVendorAccountNumber**-kentän.
    
        ![Itsenäinen tai kehäviittaus 4](media/vend-selfref4.png)
    
    5. Tallenna yhdistämismuutokset.

2. Poista **Toimittajien V2**-yksikön muutosjäljitys käytöstä.

    1. Siirry kohtaan **Tietojen hallinta \> Tietoyksiköt**.
    
    2. Valitse **Toimittajat V2**-yksikkö.
    
    3. Valitse valikkoriviltä **Asetukset** ja **Muuta seurantaa**.
    
        ![itsenäinen tai kehäviittaus 5](media/selfref_options.png)
    
    4. Valitse **Poista muutosten jäljitys käytöstä**.
    
        ![itsenäinen tai kehäviittaus 6](media/selfref_tracking.png)

3. Suorita **Toimittajien V2 (msdyn_vendors)** -määrityksen ensimmäinen synkronointi. Alkuperäisen synkronoinnin pitäisi toimia virheettä.

4. Suorita **CDS-yhteystiedot V2 (contacts)** -määrityksen ensimmäinen synkronointi. Tämä yhdistämismääritys on synkronoitava, jos haluat synkronoida toimittajien ensisijaisen yhteystietokentän, koska yhteystietotietueet on myös ensin synkronoitava.

5. Lisää kentät **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** takaisin **Toimittajat V2 (msdyn_vendors)** -kartoitukseen ja tallenna yhdistämismääritys.

6. Suorita uudelleen **Toimittajien V2 (msdyn_vendors)** -määrityksen ensimmäinen synkronointi. Kaikki tiedot synkronoidaan, koska muutosten seuranta on poistettu käytöstä.

7. Ota **Toimittajien V2** -yksikön muutosjäljitys käyttöön.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Asiakasyksikön yhdistämismäärityksen asiakkaiden V3-virheen ratkaiseminen

Saatat joutua käyttämään seuraavia alkusynkronointivirheitä kohteesta **Asiakkaat V3** kohteen **Tilit**-kartoitukseen, jos entiteeteillä on aiemmin luotuja, **ContactPersonID**- ja **InvoiceAccount** -kenttien arvoja. Tämä johtuu siitä, että **InvoiceAccount** on itseviittaava kenttä ja **ContactPersonID** on kehäviittaus toimittajan yhdistämismäärityksessä.

*Kentän GUID-arvon selvittäminen ei onnistunut: <field>. Hakua ei löydy: <value>. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *Kentän GUID-arvon selvittäminen ei onnistunut: primarycontactid.msdyn_contactpersonid. Hakua ei löydy: 000056. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Kentän GUID-arvon selvittäminen ei onnistunut: msdyn_billingaccount.accountnumber. Hakua ei löydy: 1206-1. Kokeile näitä URL-osoitteita ja tarkista, ovatko viitetiedot olemassa: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

Jos asiakasyksikön kentissä on arvoja, joiden arvot ovat samat, suorita ensimmäinen synkronointi onnistuneesti noudattamalla alla olevan kohdan ohjeita. Tämän menetelmän avulla voit käyttää kaikkia tällaisia tilejä ja yhteyshenkilöitä.

1. Poista Finance and Operations -sovelluksessa **ContactPersonID**- ja **InvoiceAccount** -kentät **Asiakkaat V3 (accounts)** -määrityksestä ja tallenna määritys.

    1. Siirry toimittajat-version **Asiakkaat V3 (accounts)** -kaksoiskirjoitusmääritysten sivulle ja valitse **yksiköiden yhdistämismääritykset** -välilehti. Valitse vasemmanpuoleisesta suodattimesta **Finance and Operations -sovellukset. Asiakkaat V3**. Valitse oikeanpuoleisesta suodattimesta **Common Data Service.Account**.

    2. Katso **contactperson** ja etsi lähdekenttä **ContactPersonID**.
    
    3. Napsauta **Toiminnot**-painiketta ja valitse **Poista**.
    
        ![Itsenäinen tai kehäviittaus 3](media/cust_selfref3.png)
    
    4. Poista uudelleen, jos haluat poistaa **IInvoiceAccount**-kentän.
    
        ![Itsenäinen tai kehäviittaus](media/cust_selfref4.png)
    
    5. Tallenna yhdistämismuutokset.

2. Poista **Asiakkaiden V3**-yksikön muutosjäljitys käytöstä.

    1. Siirry kohtaan **Tietojen hallinta \> Tietoyksiköt**.
    
    2. Valitse **Asiakkaat V3**-yksikkö.
    
    3. Valitse valikkoriviltä **Asetukset** ja **Muuta seurantaa**.
    
        ![itsenäinen tai kehäviittaus 5](media/selfref_options.png)
    
    4. Valitse **Poista muutosten jäljitys käytöstä**.
    
        ![itsenäinen tai kehäviittaus 6](media/selfref_tracking.png)

3. Suorita **Asiakkaat V3 (Accounts)** -määrityksen ensimmäinen synkronointi. Alkuperäisen synkronoinnin pitäisi toimia virheettä.

4. Suorita **CDS-yhteystiedot V2 (contacts)** -määrityksen ensimmäinen synkronointi. Samalla nimellä on 2 karttaa. Valitse se, jolla on kuvauksen **Kaksoiskirjoitusmalli synkronointiin FO.CDS Toimittajayhteyshenkilöiden V2 ja CDS.Contacts välillä. Vaatii uutta pakettia. \[Dynamics365SupplyChainExtended\] .** Kartan **Tiedot**-välilehdessä.

5. Lisää **InvoiceAccount**- ja **ContactPersonId** -kentät **Asiakkaat V3 (accounts)** -määrityksestä ja tallenna määritys. Nyt sekä **InvoiceAccount**-kenttä että **ContactPersonId**-kenttä ovat jälleen osa live sync -tilaa. Seuraavassa vaiheessa näiden kenttien ensimmäinen synkronointi on valmis.

6. Suorita uudelleen **Asiakkaat V3 (Accounts)** -määrityksen ensimmäinen synkronointi. Koska muutosten seuranta on poistettu käytöstä, synkronoinnin suoritus synkronoi **InvoiceAccount**- ja **ContactPersonId** -tiedot Finance and Operations -sovelluksesta Common Data Service -sovellukseen.

7. Voit synkronoida **InvoiceAccount**- ja **ContactPersonId** -tiedot Common Data Service -järjestelmästä Finance and Operationsiin käyttämällä tietojen integrointiprojektia.

    1. Luo Power Appsissa tietojen integrointiprojekti **Sales.Account**- ja **Finance and Operations apps.Customers V3** -entiteettien välille. Tietojen suunnan on oltava peräisin Common Data Servicestä Finance and Operations -sovellukseen.  Koska **InvoiceAccount** on uusi määrite kaksoiskirjoituksessa, tämän määritteen ensimmäinen synkronointi kannattaa ohittaa. Lisätietoja on kohdassa [Tietojen integrointi Common Data Service -ratkaisuun](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Seuraavassa kuvassa näkyy projekti, joka päivittää **CustomerAccount**- ja **ContactPersonId**-tunnukset.

        ![Itsenäinen tai kehäviittaus](media/cust_selfref6.png)

    2. Lisää yrityksen ehdot suodattimen Common Data Service -sivulle, koska vain suodatusehtoja vastaavat tiedot päivitetään Finance and Operations -sovelluksessa. Voit lisätä suodattimen napsauttamalla suodatinkuvaketta. **Muokkaa kyselyä** -valintaikkunassa voit lisätä suodatinkyselyn, kuten **_msdyn_company_value eq '\<guid\>'**. Jos suodatinkuvake ei ole näkyvissä, luo tukipyyntö, jotta tietojen integrointiryhmä voi ottaa suodattimen käyttöön vuokraajalla. Jos et määritä suodatinkyselyä kohteelle **_msdyn_company_value**, kaikki tiedot synkronoidaan.

        ![Itsenäinen tai kehäviittaus](media/cust_selfref7.png)

        Tällöin tietueen ensimmäinen synkronointi on valmis.

8. Ota käyttöön **Asiakkaiden V3**-yksikön muutosjäljitys Finance and Operations -sovelluksessa.

