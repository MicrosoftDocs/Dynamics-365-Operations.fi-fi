---
title: Mobiililaskujen hyväksynnät
description: Tämä aihe on tarkoitettu antamaan käytännön lähestymistavan Dynamics 365 for Finance and Operationsin mobiiliskenaarioiden suunnitteluun ottamalla toimittajan laskujen mobiilihyväksynnän esimerkkitapaukseksi.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5a48ea7b0c1faf5726de21a246e3d8b4d98f166a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1511657"
---
# <a name="mobile-invoice-approvals"></a>Mobiililaskujen hyväksynnät

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operationsin mobiiliominaisuuksien avulla liiketoimintakäyttäjät voivat suunnitella mobiilin käyttökokemuksen. Vaativimmissa skenaarioissa ympäristö sallii myös, että kehittäjät laajentavat ominaisuuksia kuin haluavat. Tehokkain keino oppia joitakin uusia käsitteitä mobiiliympäristössä on käydä läpi joitakin suunnittelutilanteita. Tämä aihe on tarkoitettu antamaan käytännön lähestymistavan mobiiliskenaarioiden suunnitteluun ottamalla toimittajan laskujen mobiilihyväksynnän esimerkkitapaukseksi. Tämä ohjeaihe auttaa sinua suunnittelemaan tilanteen muita variaatioita ja sitä voidaan soveltaa myös muihin tilanteisiin, jotka eivät liity toimittajan laskuihin.

<a name="prerequisites"></a>Edellytykset
-------------

| Edellytys                                                                                            | kuvaus                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobiilikäsikirja esitiedoiksi                                                                                |[Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| Dynamics 365 for Finance and Operations                                                                             | Ympäristö, johon on asennettu Microsoft Dynamics 365 for Operationsin versio 1611 ja Microsoft Dynamics for Operations platform update 3 (marraskuu 2016)                   |
| Asenna hotfix-korjaus KB 3204341.                                                                              | Tehtävän tallennus voit virheellisesti tallentaa kaksi avattavan luettelon Sulje-komentoa. Tämä sisältyy Dynamics 365 for Operationsin ympäristöpäivitykseen 3 (marraskuun 2016 päivitys) |
| Asenna hotfix-korjaus KB 3207800.                                                                              | Tämän päivityksen avulla liitteitä voi tarkastella mobiiliasiakkaassa. Tämä sisältyy Dynamics 365 for Operationsin ympäristöpäivitykseen 3 (marraskuun 2016 päivitys)           |
| Asenna hotfix-korjaus KB 3208224.                                                                              | Sovelluskoodi toimittajan laskujen hyväksynnän mobiilisovellukselle. Tämä sisältyy Microsoft Microsoft Dynamics AX -sovellukseen 7.0.1 (toukokuu 2016).                          |
| Android-, iOS- tai Windows-laite, jossa on asennettuna Finance and Operationsin mobiilisovellus | Etsi sovellus omasta sovelluskaupastasi.                                                                                                                     |

## <a name="introduction"></a>Johdanto
Toimittajalaskujen mobiilihyväksyntä vaatii nämä kolme hotfix-korjausta, jotka on mainittu "Edellytykset"-osassa. Nämä hotfix-korjaukset eivät tarjoa työtilaa laskujen hyväksyntään. Perustiedot työtiloista mobiiliympäristössä on mobiilikäsikirjassa, joka mainitaan "Edellytykset"-osassa. Laskun hyväksynnän työtila on suunniteltava. 

Jokainen organisaatio määrittää oman toimittajan laskujen liiketoimintaprosessinsa eri tavalla. Ennen kuin suunnittelet toimittajan laskujen hyväksynnän mobiilikäyttöliittymän, sinun kannattaa harkita seuraavia näkökohtia liiketoimintaprosesseista. Ajatuksena on käyttää näitä tietopisteitä mahdollisimman paljon laitteen käyttäjäkokemuksen parantamiseksi.

-   Mitkä laskun otsikon kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?
-   Mitkä laskurivien kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?
-   Kuinka monta laskuriviä yhdessä laskussa on? Käytä tässä 80-20-sääntö ja optimoi tärkeimmät 80 prosenttia.
-   Haluavatko käyttäjät tarkastella mobiililaitteessa kirjanpidollisia jakoja (laskujen koodausta) tarkistusten aikana? Jos vastaus tähän kysymykseen on kyllä, harkitse seuraavia kysymyksiä:
    -   Kuinka monta kirjanpidollista jakoa (laajennettua hintaa, arvonlisäveroa, kulua, jakoa jne.) on yhdellä laskurivillä? Käytä uudelleen 80-20-sääntöä.
    -   Onko laskuissa myös kirjanpidolliset jaot laskuotsikossa? Jos näin on, ovatko nämä kirjanpidolliset jaot on käytettävissä laitteessa?

> [!NOTE]
> Tässä ohjeaiheessa ei kerrota, kuinka muokkaa kirjanpidon jakoja, koska tätä toimintoa ei tueta tällä hetkellä mobiiliskenaarioissa.

-   Haluavatko käyttäjät nähdä laskun liitteet laitteella?

Laskun hyväksyntöjen mobiilikokemuksen rakenne vaihtelee riippuen vastauksista näihin kysymyksiin. Tavoitteena on optimoida organisaation liiketoimintaprosessin mobiilikäyttökokemus. Aiheen loppuosassa tarkastelemme kahta skenaarion versiota, jotka perustuvat eri vastauksiin edellisiin kysymyksiin. 

Yleisenä ohjeena voi sanoa, että kun työskentelet mobiilisuunnittelijan kanssa, muista julkaista muutokset, jotta päivityksiä ei menetettäisi.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Yksinkertaisen laskun hyväksynnän skenaarion suunnitteleminen Contosolle
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skenaarion määrite</th>
<th>Vastaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mitkä laskun otsikon kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</td>
<td><ol>
<li>Toimittajan nimi</li>
<li>Laskun kokonaissumma</li>
<li>Laskutusasiakasnumero</li>
<li>Laskun numero</li>
<li>Laskun päivämäärä</li>
<li>Laskun kuvaus</li>
<li>Eräpäivä</li>
<li>Laskutusvaluutta</li>
</ol></td>
</tr>
<tr class="even">
<td>Mitkä laskurivien kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</td>
<td><ol>
<li>Hankintaluokka</li>
<li>Määrä</li>
<li>Yksikköhinta</li>
<li>Rivin nettosumma</li>
<li>Valmisteveron määrä</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kuinka monta laskuriviä yhdessä laskussa on? Käytä tässä 80-20-sääntö ja optimoi tärkeimmät 80 prosenttia.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Haluavatko käyttäjät tarkastella mobiililaitteessa kirjanpidollisia jakoja (laskujen koodausta) tarkistusten aikana?</td>
<td>Kyllä</td>
</tr>
<tr class="odd">
<td>Kuinka monta kirjanpidollista jakoa (laajennettua hintaa, arvonlisäveroa, kulua jne.) on yhdellä laskurivillä? Käytä uudelleen 80-20-sääntöä.</td>
<td>Laajennettu hinta: 2 ALV: 0 Kulut: 0</td>
</tr>
<tr class="even">
<td>Onko laskuissa myös kirjanpidolliset jaot laskuotsikossa? Jos näin on, ovatko nämä kirjanpidolliset jaot on käytettävissä laitteessa?</td>
<td>Ei käytössä</td>
</tr>
<tr class="odd">
<td>Haluavatko käyttäjät nähdä laskun liitteet laitteella?</td>
<td>Kyllä</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Luo työtila

1.  Avaa selaimessa Finance and Operations ja kirjaudu sisään.
2.  Kun olet kirjautunut sisään, lisää **&mode=mobile** URL-osoitteeseen (kuten seuraavassa esimerkissä) ja päivitä sivu: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**
3.  Valitse **Asetukset** (ratas) -painike oikeassa yläkulmassa ja valitse sitten **Mobiilisovellus**. Mobiilisovelluksen suunnitteluohjelma pitäisi tulla näkyviin samoin kuin tehtävän tallennustoiminto.
4.  Luo uusi työtila napsauttamalla **Lisää**. Kirjoita tässä esimerkissä työtilan nimeksi **Omat hyväksynnät**.
5.  Anna kuvaus.
6.  Valitse työtilan väri. Työtilan väriä käytetään tämän työtilan yleisenä tyylinä mobiilikokemuksessa.
7.  Valitse työtilan kuvake.
8.  Valitse **Valmis**
9.  Tallenna muutokset valitsemalla **Julkaise työtila**

### <a name="vendor-invoices-assigned-to-me"></a>Minulle määritetyt toimittajien laskut

Ensimmäinen mobiilisivu, joka tulee suunnitella, on luettelo laskuista, jotka on määritetty käyttäjälle tarkistettavaksi. Voit suunnitella tämän mobiilisivun Finance and Operationsin **VendMobileInvoiceAssignedToMeListPage**-sivulla. Ennen kuin suoritat nämä toimet, varmista, että vähintään yksi toimittajalasku on määritetty itsellesi tarkistettavaksi, ja että laskurivillä on kaksi jakoa. Tämä määritys täyttää tämän skenaarion vaatimukset.

1.  Korvaa Finance and Operationsin URL-osoitteessa valikkovaihtoehdon nimi merkkijonolla **VendMobileInvoiceAssignedToMeListPage**, jos haluat avata **Minulle määritetyt odottavat toimittajan laskut** -luettelosivun mobiiliversion **Ostoreskontra**-moduulissa. Tässä sivussa näkyvät ne laskut, jotka on järjestelmässä liitetty sinulle. Voit etsiä tietyn laskun käyttämällä suodatinta vasemmalla puolella. Kuitenkaan tässä esimerkissä ei edellytetä tiettyä laskua. Tarvitset vain jonkin sinulle määritetyn laskun, jonka avulla voit suunnitella mobiilisivun. Käytettävissä olevat uudet sivut on suunniteltu erityisesti kehittämään mobiiliskenaarioita toimittajalaskuille. Siksi sinun on käytettävä näitä sivuja. URL-osoitteen pitäisi olla samantyyppinen seuraavan osoitteen kanssa, ja siihen siirryttyäsi sinun pitäisi nähdä oheisen kuvan mukainen sivu: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Minulle määritettyjen odottavien toimittajalaskujen luettelosivu](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Valitse **Asetukset** (ratas) -painike oikeassa yläkulmassa ja valitse sitten **Mobiilisovellus**.
3.  Valitse työtila ja sitten **Muokkaa**
4.  Valitse **Lisää sivu** luodaksesi ensimmäisen mobiilisivun.
5.  Kirjoita nimi, kuten **Omat toimittajalaskut** sekä kuvaus, kuten **Minulle tarkistettavaksi määritetyt toimittajalaskut**.
6.  Valitse **Valmis**.
7.  Valitse mobiilisivujen suunnitteluohjelmassa **Kentät**-välilehdessä **Valitse kentät**. Luettelosivun sarakkeiden tulisi olla likipitäen kuin seuraavassa kuvassa. [![Sarakkeet Minulle määritetyt odottavat toimittajan laskut -sivulla](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Lisää tarvittavat sarakkeet luettelosivulta, joka on näytettävä käyttäjille mobiilisivulla. Kentät näytetään loppukäyttäjille lisäämisjärjestyksessä. Ainoa tapa muuttaa kenttien järjestystä on valita kaikki kentät uudelleen. Tämän skenaarion vaatimusten mukaan seuraavat kahdeksan kenttää ovat pakollisia. Joidenkin käyttäjien mielestä kahdeksan kenttää mobiililaitteessa saattaa kuitenkin olla liikaa. Siksi näytämme vain tärkeimmät kentät mobiilissa luettelonäkymässä. Muut kentät näkyvät tietonäkymässä, jonka suunnittelemme myöhemmin. Nyt lisäämme seuraavat kentät. Napsauta plus-merkkiä (**+**) sarakkeissa lisätäksesi ne mobiilisivulle.
    - Toimittajan nimi
    - Laskun kokonaissumma
    - Laskutusasiakasnumero
    - Laskun numero
    - Laskun päivämäärä

    Kun kentät on lisätty, mobiilisivun pitäisi muistuttaa seuraavaa kuvaa. 
    [![Sivu kenttien lisäämisen jälkeen](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  On myös lisättävä seuraavat sarakkeet nyt, että voimme ottaa työnkulkutoimintoja myöhemmin käyttöön.
    - Näytä Suorita-tehtävä
    - Näytä Delegoi-tehtävä
    - Näytä Peruuta-tehtävä
    - Näytä Hylkää-tehtävä
    - Näytä Pyydä suoritusta -tehtävä
    - Näytä Lähetä uudelleen -tehtävä

10. Valitse **Valmis** poistuaksesi muokkaustilasta.
11. Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.
12. Tallenna muutokset valitsemalla **Julkaise työtila**.
13. Ota käyttöön **Näytä laskun loppusumma odottavien toimittajalaskujen luettelossa** Ostoreskontran parametrit -lomakkeessa kohdassa **Lasku**. Huomaa, että ainoastaan ottamalla käyttöön tämän parametrin laskun kokonaissumma lasketaan näytettäväksi odottavien toimittajan laskujen luettelosivulla. Tämä on uusi ominaisuus, joka kuuluu vaadittuun hotfix-korjaukseen 3208224.

### <a name="vendor-invoice-details"></a>Toimittajan laskun tiedot

Voit suunnitella laskun tietojen sivun käyttämällä Finance and Operationsin **VendMobileInvoiceHeaderDetails**-sivua. Huomaa, että riippuen järjestelmässäsi olevien laskujen määrästä tällä sivulla näytetään vanhin lasku (lasku, joka on luotu ensin). Voit etsiä tietyn laskun käyttämällä suodatinta vasemmalla puolella. Kuitenkaan tässä esimerkissä ei edellytetä tiettyä laskua. Tässä tarvitaan vain jotkin laskutiedot, että voimme suunnitella mobiilisivun. [![Työnkulku-sivu](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1. Korvaa Finance and Operationsin URL-osoitteessa valikkovaihtoehto nimi merkkijonolla **VendMobileInvoiceHeaderDetails**, jos haluat avata lomakkeen
2. Avaa mobiilisivujen suunnitteluohjelma **Asetukset** (ratas) -painikkeesta.
3. Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.
4. Valitse **Omat toimittajalaskut** -sivu, jonka loit aiemmin ja valitse sitten **Muokkaa**.
5. Valitse **Kentät** -välilehdessä sarakkeen otsikko **Ruudukko**.
6. Valitse **Ominaisuudet &gt; Lisää sivu**. **Huomautus:** Kun valitset **Ruudukko**-otsikon ja lisäät sivun, yhteys tietosivuun muodostetaan automaattisesti.
7. Kirjoita sivun otsikko, esimerkiksi **Laskun tiedot** ja kuvaus, kuten **Näytä laskun otsikko ja rivitiedot**.
8. Klikkaa **Valitse kentät**. Huomaa, että kentät näytetään loppukäyttäjille lisäämisjärjestyksessä. Ainoa tapa muuttaa kenttien järjestystä on valita kaikki kentät uudelleen. 
9. Lisää seuraavat kentät otsikosta tämän skenaarion vaatimusten mukaan:
   - Toimittajan nimi
   - Laskun kokonaissumma
   - Laskutusasiakasnumero
   - Laskun numero
   - Laskun päivämäärä
   - Laskun kuvaus
   - Eräpäivä
   - Laskutusvaluutta

10. Lisää seuraavat kentät sivun riviruudukosta:
    - Hankintaluokka
    - Määrä
    - Yksikköhinta
    - Rivin nettosumma
    - Valmisteveron määrä

11. Kun kaikki edellisten kahden vaiheen kentät on lisätty, valitse **Valmis**. Sivun tulisi olla likipitäen kuin seuraavassa kuvassa.
    [![Sivu kenttien lisäämisen jälkeen](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Valitse **Valmis** poistuaksesi muokkaustilasta.
13. Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.
14. Tallenna muutokset valitsemalla **Julkaise työtila**.

### <a name="workflow-actions"></a>Työnkulkutehtävät

Voit lisätä työnkulkutoimintoja Finance and Operationsin **VendMobileInvoiceHeaderDetails**-sivulla. Jos haluat avata tämän sivun, korvaa valikkovaihtoehdon nimi URL-osoitteessa, kuten teit aikaisemmin. Avaa sitten mobiilisivujen suunnitteluohjelma **Asetukset** (ratas) -painikkeesta. Toimi seuraavien vaiheiden mukaisesti lisätäksesi työnkulkutoimintoja tietosivulle. Sinulle on oltava määritettynä sopivassa tilassa olevia laskuja, joiden avulla pääset työnkulkutoimintoihin.

#### <a name="record-workflow-actions"></a>Työnkulkutoimintojen tallentaminen
1.  Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.
2.  Valitse **Laskun tiedot** -sivu, jonka loit aiemmin ja valitse sitten **Muokkaa**.
3.  Valitse **Toiminnot**-välilehdessä **Lisää toiminto**.
4.  Kirjoita toiminnon otsikko, esimerkiksi **Hyväksy** ja kuvaus, kuten **Hyväksy lasku**. Huomaa, että tässä antamasi otsikko näkyy loppukäyttäjille toiminnon nimenä mobiilisovelluksessa.
5.  Valitse **Valmis**.
6.  Klikkaa **Valitse kentät**.
7.  Siirry työnkulkuprosessin kautta **VendMobileInvoiceHeaderDetails**-sivulle ja suorita toiminto, jonka haluat tallentaa. Varmista, että kirjoitat työnkulun kommentit tämän prosessin aikana, jotta kommenttikenttä sisältyy myös mobiilikokemukseen.
8.  Kun työnkulkutoiminto on suoritettu, valitse **Valmis** viimeistelläksesi Valitse kentät -tehtävän.
9.  Valitse **Valmis** poistuaksesi muokkaustilasta.
10. Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.
11. Tallenna muutokset valitsemalla **Julkaise työtila**.
12. Tallenna kaikki tarvittavat työnkulkutoiminnot toistamalla edelliset vaiheet. 

#### <a name="create-a-js-file"></a>.js-tiedoston luominen
1. Avaa Muistio tai Microsoft Visual Studio ja liitä seuraava koodi. Tallenna tiedosto .js-tiedostona. Koodilla voidaan suorittaa seuraavia toimintoja:
    - Se piilottaa ylimääräiset työnkulkuun liittyvät sarakkeet, jotka on lisätty aiemmin mobiililuettelosivulla. Lisäsimme nämä sarakkeet, jotta sovelluksella on nämä tiedot oikeassa asiayhteydessä, jotta se voi suorittaa seuraavan vaiheen.
    - Aktiiviseen työnkulun vaiheen perusteella se käyttää logiikkaa, joka näyttää vain kyseiset toiminnot.

> [!NOTE]
> Sivujen ja muiden ohjausobjektien nimet on oltava koodissa samat kuin työtilan nimet.

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  Lataa kooditiedoston työtilaan valitsemalla **Logiikka**-välilehti
3.  Valitse **Valmis** poistuaksesi muokkaustilasta.
4.  Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.
5.  Tallenna muutokset valitsemalla **Julkaise työtila**.

### <a name="vendor-invoice-attachments"></a>Toimittajalaskujen liitteet

1. Valitse **Asetukset** (ratas) -painike oikeassa yläkulmassa ja valitse sitten **Mobiilisovellus**.
2. Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.
3. Valitse <strong>Laskun tiedot **-sivu, jonka loit aiemmin ja valitse sitten **Muokkaa</strong>.
4. Määritä **Tiedostojen hallinta** -asetukseksi **Kyllä** alla olevan esimerkin mukaisesti. **Huomautus:** Jos ei ole liitteitä ei ole tarpeen näyttää mobiililaitteessa, voit jättää tämän vaihtoehdon arvoksi **Ei**, joka on oletusasetus.
   ![Tiedoston hallinta](./media/docmanagement-216x300.png)
5. Valitse **Valmis** poistuaksesi muokkaustilasta.
6. Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.
7. Tallenna muutokset valitsemalla **Julkaise työtila**.

### <a name="vendor-invoice-line-distributions"></a>Toimittajan laskujen rivijaot

Tämän skenaarion vaatimukset vahvistavat, että seillä on vain rivitason jaot ja että laskulla on aina vain yksi rivi. Koska tämä skenaario on yksinkertainen, mobiililaitteen käyttökokemuksenkin täytyy olla yksinkertainen, jotta käyttäjän ei tarvitse porautua alaspäin useita tasoja nähdäkseen jaot. Finance and Operationsin toimittajan laskuihin sisältyy mahdollisuus näyttää kaikki jaot laskun otsikosta. Tämän kokemuksen tarvitsemme mobiiliskenaariossa. Tämän vuoksi käytämme **VendMobileInvoiceAllDistributionTree**-sivua suunnittellaksemme mobiiliskenaarion tämän osan. 

> [!NOTE] 
> Kun tiedämme vaatimukset, se auttaa päättämään, mitä tiettyä sivua käyttää ja miten tarkalleen optimoida käyttäjän mobiilikokemus, kun suunnittelemme tätä skenaariota. Toisessa tilanteessa käytämme toista sivua näyttämään jaot, koska skenaarioiden vaatimukset eroavat.

1.  Korvaa valikkovaihtoehdon nimi URL-osoitteessa, kuten teit aikaisemmin. Sivun, joka näkyy, on muistutettava seuraavaa kuvaa.
[![Kaikki jaot -sivu](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Avaa mobiilisivujen suunnitteluohjelma **Asetukset** (ratas) -painikkeesta.
3.  Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa. **Huomautus:** Näet, että kaksi uutta sivua on luotu automaattisesti. Järjestelmä luo nämä sivut, koska otit käyttöön tiedostojen hallinnan edellisessä osassa. Voit ohittaa nämä uudet sivut.
4.  Valitse **Lisää sivu**.
5.  Kirjoita sivun otsikko, esimerkiksi **Näytä kirjanpito**  ja kuvaus, kuten **Näytä laskun kirjanpito**.
6.  Valitse **Valmis**.
7.  Klikkaa **Kentät**-välilehdessä **Valitse kentät**, valitse seuraavat kentät Jaot-sivulta ja valitse sitten **Valmis**:
    1.  Summa
    2.  Valuutta
    3.  Kirjanpitotili

    > [!NOTE] 
    > Emme valinneet **Kuvaus**-saraketta jakoruudukosta, koska tämän skenaarion vaatimukset vahvistivat, että vain laajennetulle hinnalle on olemassa jako. Tämän vuoksi käyttäjä ei edellytä toista kenttää sen summan tyypin määrittämiseksi, jolle jako on. Kuitenkin seuraavassa skenaariossa me **tulemme** käyttämään tätä tietoa, koska tämän skenaarion vaatimukset määrittävät, että muuntyyppisilläkin summilla on jakoja (kuten arvonlisävero).
8.  Valitse **Valmis** poistuaksesi muokkaustilasta.
9.  Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.
10. Tallenna muutokset valitsemalla **Julkaise työtila**.

> [!NOTE] 
> **Näytä kirjanpito** -mobiilisivua ei ole tällä hetkellä linkitetty yhteenkään tähän mennessä suunniteltuun mobiilisivuun. Koska käyttäjän pitää voida siirtyä **Näytä kirjanpito** -sivulle mobiililaitteen **Laskun tiedot** -sivulta, meidän on luotava siirtyminen **Laskun tiedot** -sivulta **Näytä kirjanpito** -sivulle. Luomme tämän siirtymisen JavaScript-lisälogiikan avulla.

1.  Avaa .js-tiedosto, jonka loit aiemmin ja lisää rivit, jotka näkyvät korostettuina seuraavassa koodissa. Tämä koodi tekee kaksi asiaa:
    1.  Sen avulla varmistetaan, että käyttäjät eivät voi siirtyä suoraan työtilasta **Näytä kirjanpito** -sivulle.
    2.  Se luo siirtymisen ohjausobjektin **Laskun tiedot** -sivulta **Näytä kirjanpito** -sivulle.

> [!NOTE] 
> Sivujen ja muiden ohjausobjektien nimet on oltava koodissa samat kuin työtilan nimet.

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  Lataa kooditiedosto työtilaan ja korvaa edellinen koodi valitsemalla **Logiikka**-välilehti
3.  Valitse **Valmis** poistuaksesi muokkaustilasta.
4.  Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.
5.  Tallenna muutokset valitsemalla **Julkaise työtila**.

### <a name="validation"></a>Valintasäännöt

Avaa sovellus mobiililaitteessa ja muodosta yhteys Finance and Operations -esiintymään. Varmista, että kirjaudut yritykseen jossa toimittajalaskuja on määritetty sinulle tarkistusta varten. Sinun pitäisi voida suorittaa seuraavat toimet:

-   Nähdä **Omat hyväksynnät** -työtila.
-   Porautua **Omat hyväksynnät** -työtilaan ja nähdä **Omat toimittajalaskut** -sivun.
-   Porautua **Omat toimittajalaskut** -sivulle ja nähdä sinulle määritetyt laskut.
-   Poraudu yhteen laskuista ja tarkastele laskun otsikon ja rivien tietoja.
-   Tiedot-sivulla näet linkin liitteisiin ja tämän linkin avulla voit siirtyä liiteluetteloon ja tarkastella liitteitä.
-   Tiedot-sivulla näet linkin **Näytä kirjanpito** -sivulle ja tämän linkin avulla voit siirtyä jakosivulle ja tarkastella jakoja.
-   Valitse Tiedot-sivulla **Toiminnot**-valikko sivun alaosasta ja suorita työnkulkutoimintoja, joita sovelletaan työnkulun vaiheeseen.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Monimutkaisen laskun hyväksynnän skenaarion suunnitteleminen Fabrikamille
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skenaarion määrite</th>
<th>Vastaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mitkä laskun otsikon kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</td>
<td><ol>
<li>Toimittajan nimi</li>
<li>Laskun summa</li>
<li>Laskutusasiakasnumero</li>
<li>Laskun numero</li>
<li>Laskun päivämäärä</li>
<li>Laskun kuvaus</li>
<li>Eräpäivä</li>
<li>Laskutusvaluutta</li>
</ol></td>
</tr>
<tr class="even">
<td>Mitkä laskurivien kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</td>
<td><ol>
<li>Hankintaluokka</li>
<li>Määrä</li>
<li>Yksikköhinta</li>
<li>Rivin nettosumma</li>
<li>Valmisteveron määrä</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kuinka monta laskuriviä yhdessä laskussa on? Käytä tässä 80-20-sääntö ja optimoi tärkeimmät 80 prosenttia.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Haluavatko käyttäjät tarkastella mobiililaitteessa kirjanpidollisia jakoja (laskujen koodausta) tarkistusten aikana?</td>
<td>Kyllä</td>
</tr>
<tr class="odd">
<td>Kuinka monta kirjanpidollista jakoa (laajennettua hintaa, arvonlisäveroa, kulua jne.) on yhdellä laskurivillä? Käytä uudelleen 80-20-sääntöä.</td>
<td>Laajennettu hinta: 2 ALV: 2 Kulut: 2</td>
</tr>
<tr class="even">
<td>Onko laskuissa myös kirjanpidolliset jaot laskuotsikossa? Jos näin on, ovatko nämä kirjanpidolliset jaot on käytettävissä laitteessa?</td>
<td>Ei käytössä</td>
</tr>
<tr class="odd">
<td>Haluavatko käyttäjät nähdä laskun liitteet laitteella?</td>
<td>Kyllä</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>Seuraavat vaiheet

Skenaariolle 1 voidaan tehdä seuraavat muunnelmat perustuen skenaarion 2 vaatimuksiin. Voit parantaa mobiilisovelluskokemusta tämän osan avulla.

1.  Koska skenaariossa 2 odotetaan enemmän laskurivejä, seuraavat muutokset rakenteeseen auttavat optimoimaan mobiililaitteen käyttökokemusta:
    1.  Sen sijaan että tarkastelisit laskurivejä tietosivulla (kuten skenaariossa 1), käyttäjät voivat tarkastella rivejä erillisellä mobiilisivulla.
    2.  Koska tässä tilanteessa on odotettavissa useita laskun rivejä ja jos **VendMobileInvoiceAllDistributionTree** -sivua käytetään mobiilin jakosivun suunnittelussa (kuten skenaariossa 1), se voi olla hämmentävää käyttäjälle yhdistää rivit jakoihin. Tämän vuoksi käytä **VendMobileInvoiceLineDistributionTree**-sivua jakosivun suunnitteluun.
    3.  Parhaassa tapauksessa tässä skenaariossa jaot pitäisi näyttää laskurivin yhteydessä. Varmista siksi, että käyttäjä voi porautua riviin nähdäkseen jakosivun. Sivulinkkiominaisuuden avulla voit määrittää porautumisen samalla tavalla kuin otsikko- ja tietosivuille skenaariossa 1.

2.  Koska skenaariossa 2 on odotettavissa useita summatyyppejä (arvonlisävero, kulut jne.), on hyödyllistä näyttää summatyypin kuvaus. (Nämä tiedot jätettiin pois skenaariossa 1).




