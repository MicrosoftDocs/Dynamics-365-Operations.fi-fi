---
title: "Nuolet-lasku hyväksynnät"
description: "Microsoft Dynamics-365 työvaiheiden kannettavien ominaisuudet antaa business käyttäjän suunnitella mobiili kokemuksia. On tietoja vaativammista skenaarioista ympäristö myös oletetaan, että kehittäjät laajentavat ominaisuuksia kuin haluavat. Tehokkain keino oppia joitakin uusia käsitteitä Mobile on käydä läpi joitakin tilanteita suunniteltaessa. Tämä aihe on tarkoitettu antamaan käytännön lähestymistapaa ottamalla toimittajan laskujen hyväksyntiä käyttötapaukseen kuin mobiili mobiili skenaarioita suunnitteleminen. Tämä ohjeaihe auttaa sinua suunnitella tilanteissa muut variaatiot ja voidaan soveltaa myös muita tilanteita, jotka eivät liity toimittajan laskuihin."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Nuolet-lasku hyväksynnät

Microsoft Dynamics-365 työvaiheiden kannettavien ominaisuudet antaa business käyttäjän suunnitella mobiili kokemuksia. On tietoja vaativammista skenaarioista ympäristö myös oletetaan, että kehittäjät laajentavat ominaisuuksia kuin haluavat. Tehokkain keino oppia joitakin uusia käsitteitä Mobile on käydä läpi joitakin tilanteita suunniteltaessa. Tämä aihe on tarkoitettu antamaan käytännön lähestymistapaa ottamalla toimittajan laskujen hyväksyntiä käyttötapaukseen kuin mobiili mobiili skenaarioita suunnitteleminen. Tämä ohjeaihe auttaa sinua suunnitella tilanteissa muut variaatiot ja voidaan soveltaa myös muita tilanteita, jotka eivät liity toimittajan laskuihin.

<a name="prerequisites"></a>Edellytykset
-------------

| Edellytys                                                                                            | kuvaus                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobiili valmiiksi lukea käsikirja                                                                                |(/ dynamics365/toiminnot/dev-IT Pro/mobile-sovellukset / mobile-platform.md)                                                                                                  |
| Työvaiheiden Dynamics 365                                                                             | Päivitä-ympäristö, joka on Microsoft Dynamics-365-version toimintoja 1611 ja toimia ympäristön Microsoft Dynamics 3 (marraskuu-2016)                   |
| KB 3204341-korjaustiedoston asentaminen.                                                                              | Tehtävän tallennus voit tallentaa kahden avattavan luettelon keskusteluja tämä sisältyy Dynamics 365 toiminnon platform update (päivitys marraskuun 2016) 3 Sulje komentoja virheellisesti |
| KB 3207800-korjaustiedoston asentaminen.                                                                              | Tämän hotfix-korjauksen avulla tämä sisältyy Dynamics 365 toiminnon platform update (päivitys marraskuun 2016) 3 mobile client voidaan tarkastella liitteitä.           |
| KB 3208224-korjaustiedoston asentaminen.                                                                              | Hakemus koodi lisätään Microsoft Dynamics AX-sovelluksen 7.0.1 (toukokuussa 2016) mobiili toimittajan laskun hyväksyntää koskevasta hakemuksesta.                          |
| Android tai iOS- tai Windows-laite, joka on asennettu työvaiheiden 365 Dynamics mobile app | Etsi sopiva app store-sovelluksen.                                                                                                                     |

## <a name="introduction"></a>Johdanto
Mobiili toimittajalaskujen hyväksynnän vaativat kolme korjaukset, jotka "Edellytykset"-osassa. Nämä hotfix-korjaukset eivät tarjoa työtilan laskujen hyväksyntiä. Työtila on tietoja siitä, mitä mobiili-yhteydessä lukea mobile handbook, "Edellytykset"-osassa. Laskun hyväksynnät työtilan on suunniteltava. 

Jokaisen organisaation orchestrates ja määrittää sen toimittajan laskujen liiketoimintaprosessin eri tavalla. Ennen kuin suunnittelet käyttäjiesi tarpeiden mukaan toimittajan laskujen hyväksyntiä, sinun kannattaa harkita seuraavia näkökohtia liiketoimintaprosessin. Ajatuksena on käyttää näiden pisteiden laitteen käyttäjäkokemuksen parantamiseksi niin paljon kuin mahdollista.

-   Laskun otsikon kentät käyttäjä haluavat nähdä mobiili kokemus ja missä järjestyksessä?
-   Laskurivien kenttiä mitä käyttäjän haluat nähdä mobiili kokemus ja missä järjestyksessä?
-   Kuinka monta laskurivien onko lasku? Käytä tätä 80-20 sääntö ja optimoida 80 prosenttia.
-   Käyttäjät haluavat tarkastella mobiililaitteen kirjanpidolliset jaot (lasku coding) aikana arvostelut? Jos vastaus tähän kysymykseen on Kyllä, harkitse seuraavia kysymyksiä:
    -   Kuinka monta kirjanpidolliset jaot (Laajennettu hinta, arvonlisävero, kulut, jakaa ja niin edelleen) on laskuriviä varten? Käytä uudelleen 80-20 sääntö.
    -   Laskut myös tarvitse kirjanpidollisten jakojen ja laskuotsikon? Jos näin on, nämä kirjanpidolliset jaot on käytettävissä laitteessa?

> [!NOTE]
> Tässä ohjeaiheessa ei kerrotaan, kuinka Muokkaa kirjanpidon jakoja, koska tätä toimintoa ei tueta tällä hetkellä mobiili skenaarioita.

-   Käyttäjät haluavat nähdä laitteen laskulle liitteitä?

Laskun hyväksyntöjen mobiili kokemus rakenne vaihtelevat mukaan vastauksia näihin kysymyksiin. Tavoitteena on optimoida liiketoimintaprosessin Mobile organisaation käyttökokemusta. -Aiheen loppuosassa tarkastelemme kahden skenaarion vaihtelut, jotka perustuvat eri Edellinen kysymyksiin annettujen vastausten muodossa. 

Sellaisena kuin se yleisiä ohjeita, kun työskentelet mobiili suunnittelu muista julkaista päivityksiä säilyttää muutokset.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Contoso yksinkertaisen laskun hyväksynnän Skenaarion suunnitteleminen
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
<td>Laskun otsikon kentät käyttäjä haluavat nähdä mobiili kokemus ja missä järjestyksessä?</td>
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
<td>Laskurivien kenttiä mitä käyttäjän haluat nähdä mobiili kokemus ja missä järjestyksessä?</td>
<td><ol>
<li>Hankintaluokka</li>
<li>Määrä</li>
<li>Yksikköhinta</li>
<li>Rivin nettosumma</li>
<li>Valmisteveron määrä</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kuinka monta laskurivien onko lasku? Käytä tätä 80-20 sääntö ja optimoida 80 prosenttia.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Käyttäjät haluavat tarkastella mobiililaitteen kirjanpidolliset jaot (lasku coding) aikana arvostelut?</td>
<td>Kyllä</td>
</tr>
<tr class="odd">
<td>Kuinka monta kirjanpidolliset jaot (Laajennettu hinta, arvonlisävero, kulut ja niin edelleen) on laskuriviä varten? Käytä uudelleen 80-20 sääntö.</td>
<td>Kokonaishinta: 2 ALV: kulut 0: 0</td>
</tr>
<tr class="even">
<td>Laskut myös tarvitse kirjanpidollisten jakojen ja laskuotsikon? Jos näin on, nämä kirjanpidolliset jaot on käytettävissä laitteessa?</td>
<td>Ei käytössä</td>
</tr>
<tr class="odd">
<td>Käyttäjät haluavat nähdä laitteen laskulle liitteitä?</td>
<td>Kyllä</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Luo työtila

1.  Selaimessa Avaa Dynamics 365 operaatioille ja kirjaudu sisään.
2.  Jälkeen, kun olet kirjautunut, Liitä **& tilassa = mobiili** URL-osoitteeseen, kuten seuraavassa esimerkissä ja Päivitä sivu: https://&lt;yoururl&gt;/? cmp = usmf & mi = DefaultDashboard**& mode = mobiili**
3.  Valitse **asetukset** (vaihde)-painiketta vasemmassa yläkulmassa oikealla sivulla ja valitse sitten **Mobile app**. Suunnittelija mobile app on osoitettava samoin kuin tehtävän tallennus näkyy.
4.  Valitse **Lisää** Luo uusi työtila. Tässä esimerkissä nimi työtilan **Omat hyväksynnät**.
5.  Anna kuvaus.
6.  Valitse työtila. Työtilan väriä käytetään yleistä tyyliä tämän työtilan mobiili kokemus.
7.  Valitse työtilan kuvake.
8.  Valitse **tehty**
9.  Valitse **julkaista työtilan** Tallenna muutokset

### <a name="vendor-invoices-assigned-to-me"></a>Minulle määritetyt toimittajien laskut

Ensimmäinen mobiili-sivu, joka tulee suunnitella on luettelo laskuista, jotka on määritetty käyttäjälle tarkistettavaksi. Voit suunnitella tämän sivun mobiili- **VendMobileInvoiceAssignedToMeListPage** toiminnoissa Dynamics 365 sivua. Ennen kuin suoritat nämä toimet, varmista, että vähintään yksi toimittajalasku on määritetty itsellesi tarkistettavaksi, ja että laskurivillä on kaksi jaot. Tämä asennus täyttää tässä tilanteessa.

1.  Korvaa Dynamics 365 toimintojen URL-osoitteen, valikkokohteen nimi **VendMobileInvoiceAssignedToMeListPage** Avaa mobiili versio **minulle määritettyjen odottavien toimittajalaskujen** -sivu **Ostoreskontra** moduuli. Tässä sivussa näkyvät ne laskut laskut, jotka on järjestelmään liitetty sinulle määrän mukaan. Voit etsiä tiettyyn laskuun, voit käyttää suodatinta vasemmalla puolella. Kuitenkin olemme tässä esimerkissä eivät edellytä tiettyyn laskuun. Vain tarvitsee joitakin laskun sinulle, joka on menossa, jotta voit suunnitella Matkaviestin-sivulta. Käytettävissä olevat uudet sivut on suunniteltu erityisesti kehittää mobiili tilanteissa toimittajan laskun. Siksi sinun on käytettävä näitä sivuja. URL-Osoitteen tulee olla seuraava URL-osoite ja sen jälkeen, kun olet kirjoittanut, sivu, joka näkyy kuvassa on kirjoitettava: https://&lt;yourURL&gt;/? cmp = usmf & mi =**VendMobileInvoiceAssignedToMeListPage**& mode = mobiili [![minulle määritettyjen odottavien toimittajalaskujen sivu](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Valitse **asetukset** (vaihde)-painiketta vasemmassa yläkulmassa oikealla sivulla ja valitse sitten **Mobile app**
3.  Valitse työtilan ja **muokkaaminen**
4.  Valitse **Lisää sivulla** ensimmäinen mobiili-sivun luomiseen.
5.  Kirjoita nimi, kuten **oma toimittajalaskujen**, ja kuvaus, kuten **Tarkastele minulle määritettyjen toimittajalaskujen**.
6.  Click **Done**.
7.  Mobiili suunnittelussa- **kentät** -välilehdessä **kentät**. Sarakkeita sivulla on muistuttavat seuraavassa kuvassa. [![Sivun minulle määritettyjen odottavien toimittajalaskujen sarakkeet](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Lisää tarvittavat sarakkeet-luettelon sivulta, joka on esitettävä käyttäjille, Valitse Matkaviestin-sivulta. Joka lisää järjestys on järjestys, jossa kentät näkyvät käyttäjälle. On ainoa tapa muuttaa kenttien järjestystä valitsemalla kaikki kentät uudelleen. Tämän skenaarion vaatimusten mukaan seuraavan kahdeksan kentät ovat pakollisia. Kuitenkin jotkut käyttäjät kannattaa harkita kahdeksan kentät mobiililaitteessa on liian paljon tietoa. Siksi olemme näkyvät vain tärkeimmät kentät mobiili luettelonäkymässä. Muut kentät näkyvät tiedot-näkymä, jossa voimme suunnitella on myöhemmin. Nyt lisäämme seuraaviin kenttiin. Napsauta plus-merkkiä (**+**)-Matkaviestin-sivulta Lisää näitä sarakkeita.
    1.  Toimittajan nimi
    2.  Laskun kokonaissumma
    3.  Laskutusasiakasnumero
    4.  Laskun numero
    5.  Laskun päivämäärä

    Kun kentät on lisätty, Matkaviestin-sivulta on muistuttavat seuraavassa kuvassa. [![Kun kentät lisätään sivulle](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  On myös lisättävä seuraavat sarakkeet nyt niin, että emme Salli työnkulkutoimintoja myöhemmin.
    1.  Näytä toteuttaminen
    2.  Näytä Delegoi tehtävä
    3.  Näytä tehtävän peruuttaminen
    4.  Näytä tehtävän hylkääminen
    5.  Näytä pyyntö täydentämistehtävän.
    6.  Näytä Lähetä tehtävä

10. Valitse **tehty** Poistu muokkaustilasta.
11. Valitse **takaisin** ja **tehty** Lopeta työtilan
12. Valitse **julkaista työtilan** tallentamaan tekemäsi muutokset.
13. Ota **Näyttää laskun loppusummaan odottavien toimittajan laskujen luettelo** Ostoreskontran parametrit-lomakkeessa- **laskun**. Huomaa, että ainoastaan ottamalla käyttöön tämän parametrin, laskun summa lasketaan odottavista toimittajan laskujen sivulla näytetään. Tämä on uusi ominaisuus osana ennalta vaaditut hot Fix 3208224.

### <a name="vendor-invoice-details"></a>Toimittajan laskutustiedot

Voit suunnitella Mobile laskun tiedot-sivu, **VendMobileInvoiceHeaderDetails** toiminnoissa Dynamics 365 sivua. Huomaa että, laskut, jotka järjestelmän on määrä tällä sivulla on vanhin lasku (lasku, joka on luotu ensin). Voit etsiä tiettyyn laskuun, voit käyttää suodatinta vasemmalla puolella. Kuitenkin olemme tässä esimerkissä eivät edellytä tiettyyn laskuun. Voimme vain vaatia laskutietoja siten, että voimme suunnitella Matkaviestin-sivulta. [![Työnkulku-sivulla](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  Korvaa Dynamics 365 toimintojen URL-osoitteen, valikkokohteen nimi **VendMobileInvoiceHeaderDetails** -lomakkeen avaamiseen
2.  Avaa mobiili suunnittelu- **asetukset** (vaihde)-painiketta.
3.  Valitse **Muokkaa** käynnistääksesi muokkaustilaan työtilassa.
4.  Valitse ** Omat toimittajalaskujen **, jonka loit aiemmin sivulla ja valitse sitten **Muokkaa**.
5.  - **Kentät** -välilehdestä **ruudukon** sarakkeen otsikkoa.
6.  Valitse **ominaisuudet:**&gt;**Lisää sivulla**. **Huomautus:** kun **ruudukon** otsikko ja sivun, yhteys muodostetaan automaattisesti sivun tiedot.
7.  Kirjoita sivun otsikko, esimerkiksi **laskun tiedot**, ja kuvaus, kuten **voit tarkastella laskuotsikon ja rivin tiedot**.
8.  Valitse **kentät**. Huomaa, että, joka lisää järjestys on järjestys, jossa kentät näkyvät käyttäjälle. On ainoa tapa muuttaa kenttien järjestystä valitsemalla kaikki kentät uudelleen.
9.  Tämän skenaarion vaatimusten mukaan otsikosta Lisää seuraavat kentät:
    1.  Toimittajan nimi
    2.  Laskun kokonaissumma
    3.  Laskutusasiakasnumero
    4.  Laskun numero
    5.  Laskun päivämäärä
    6.  Laskun kuvaus
    7.  Eräpäivä
    8.  Laskutusvaluutta

10. Lisää seuraavat kentät sivun ruudukosta rivit:
    1.  Hankintaluokka
    2.  Määrä
    3.  Yksikköhinta
    4.  Rivin nettosumma
    5.  Valmisteveron määrä

11. Kun kaikki edelliset kaksi vaihetta kentät on lisätty, valitse **tehty**. Sivu on muistuttavat seuraavassa kuvassa. [![Kun kentät lisätään sivulle](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Valitse **tehty** Poistu muokkaustilasta.
13. Valitse **takaisin** ja **tehty** Lopeta työtilan
14. Valitse **julkaista työtilan** tallentaa työsi

### <a name="workflow-actions"></a>Työnkulkutehtävät

Voit lisätä työnkulkutoimintoja **VendMobileInvoiceHeaderDetails** toiminnoissa Dynamics 365 sivua. Jos haluat avata tämän sivun, korvaa URL-valikkovaihtoehdon nimi kuin teit aikaisemmin. Avaa mobiili suunnittelu- **asetukset** (vaihde)-painiketta. Toimi seuraavien vaiheiden mukaisesti voit lisätä työnkulkutoimintoja tiedot-sivulla.

1.  Valitse **Muokkaa** käynnistääksesi muokkaustilaan työtilassa.
2.  Valitse **laskun tiedot**, jonka loit aiemmin sivulla ja valitse sitten **Muokkaa**.
3.  - **Toimintojen** -välilehdessä **Lisää toiminto**.
4.  Kirjoita otsikko, esimerkiksi **Hyväksy**, ja kuvaus, kuten **Hyväksy laskun**. Huomaa, että Tässä antamasi otsikko tulee toiminnon, joka näkyy käyttäjälle mobile app nimi.
5.  Click **Done**.
6.  Valitse **kentät**.
7.  Siirry työnkulun käsittelyn kautta **VendMobileInvoiceHeaderDetails** sivulle ja suorita toiminto, jonka haluat tallentaa. Varmista, että työnkulku kommenttien syöttäminen tämän prosessin aikana niin, että kommentit-kenttään sisältyy myös mobiili kokemus.
8.  Valitse työnkulkutoiminto suoritetaan, kun **tehty** Valitse kenttiin hoidettavaksi.
9.  Valitse **tehty** Poistu muokkaustilasta.
10. Valitse **takaisin** ja **tehty** Lopeta työtilan
11. Valitse **julkaista työtilan** tallentaa työsi
12. Toista vaiheet 3 – 11-tallentaa kaikki tarvittavat työnkulkutoimintoja. Huomaa, että vaatimus on sinulle, laskut, joita voit tehdä työnkulkutoimintoja sinulle, joka aiot suunnitella tilassa.
13. Avaa Muistio tai Microsoft Visual Studio ja liitä seuraava koodi. Tallenna tiedosto nimellä .js-tiedosto. Tämä koodi tekee kaksi asiaa:
    1.  Se piilottaa ylimääräinen työnkulkuun liittyvät sarakkeet, jotka on lisätty aiemmin mobiili sivulla. Voimme lisätä nämä sarakkeet siten, että sovellus on tietojen yhteydessä ja tehdä seuraavaksi.
    2.  Perustuu työnkulun osavaiheen, joka on käytössä, se koskee näyttämään vain kyseiset toiminnot logiikan.

Huomaa, että sivut ja muiden ohjausobjektien JS-koodin on oltava sama työtilasta.

1.  Tärkein funktio (metadataService, dataService, cacheService, $q) {palauttaa {appInit: funktio (appMetadata) {/ / piilota ohjausobjektit, joiden on oltava läsnä, mutta ei näy metadataService.configureControl (' oma--toimittajalaskujen, 'ShowAccept' {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowApprove' {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowReject', {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowDelegate', {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowRequestChange', {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowRecall' {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowComplete', {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowResubmit' { piilotettu: TOSI}); }, pageInit: funktio (pageMetadata, params) {Jos (pageMetadata.Name == "Laskutustiedot") {/ / Näytä/Piilota työnkulkutoimintoja työnkulun perusteella vaihe metadataService.configureAction ('Hyväksy' {näkyvissä: TOSI}); metadataService.configureAction ('Hyväksy' {näkyvissä: TOSI}); metadataService.configureAction (Hylkää, {näkyvissä: TOSI}); metadataService.configureAction ('Edustaja' {näkyvissä: TOSI}); metadataService.configureAction (' pyynnön-muuta ', {näkyvissä: TOSI}); metadataService.configureAction ('Peruuta' {näkyvissä: TOSI}); metadataService.configureAction (kokonais, {näkyvissä: TOSI}); metadataService.configureAction ('Lähetä' {näkyvissä: TOSI});

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

2.  Ladata kooditiedoston työtilaan valitsemalla **logiikan** välilehti
3.  Valitse **tehty** Poistu muokkaustilasta.
4.  Valitse **takaisin** ja **tehty** Lopeta työtilan
5.  Valitse **julkaista työtilan** tallentaa työsi

### <a name="vendor-invoice-attachments"></a>Toimittajan laskujen liitteitä

1.  Valitse **asetukset** (vaihde)-painiketta vasemmassa yläkulmassa oikealla sivulla ja valitse sitten **Mobile app**
2.  Valitse **Muokkaa** käynnistääksesi muokkaustilaan työtilassa.
3.  Valitse ** laskun tiedot **, jonka loit aiemmin sivulla ja valitse sitten **Muokkaa**.
4.  Määrittää **tiedostojen hallinta** asetukseksi **Kyllä** alla olevan esimerkin mukaisesti. **Huomautus:** Jos ei ole Näytä liitteet kannettavan laitteen vaatimukset, voit jättää tämän vaihtoehdon arvoksi **ei**, joka on oletusasetus.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Valitse **tehty** Poistu muokkaustilasta.
7.  Valitse **takaisin** ja **tehty** Lopeta työtilan
8.  Valitse **julkaista työtilan** tallentaa työsi

### <a name="vendor-invoice-line-distributions"></a>Toimittajan laskun rivin jaot

Tämän skenaarion vaatimusten Varmista, että siellä on vain rivi-tason jaot ja, että lasku on aina vain yksi rivi. Tämä skenaario on yksinkertainen, koska käyttökokemusta kannettavan laitteen täytyy myös olla yksinkertainen niin, että käyttäjällä ei ole Poraudu alaspäin useita tasoja voit tarkastella jakoja. Toimittajalaskujen Dynamics 365 toimintoihin kuuluvat Näyttää laskun ylätunnisteeseen jaot. Tämä on mitä tarvitsemme mobiili tilanteessa. Tämän vuoksi Käytämme **VendMobileInvoiceAllDistributionTree** sivun suunnitteluun mobiili tilanteessa tässä osassa. 

> [!NOTE] 
> Tietäen vaatimukset auttaa meitä päättää, mitä käyttää ja miten tarkalleen voit optimoida käyttäjän mobiili kokemus, kun Emme suunnittele skenaario tietylle sivulle. Toisessa tilanteessa Käytämme toiselle sivulle osoittamaan jaot, koska skenaarion vaatimukset eroavat.

1.  Korvaa URL-nimi hiiren kuin teit ennen. Sivu, joka näkyy olisi muistuttavat seuraavassa kuvassa. [![Kaikki jakelut sivu](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Avaa mobiili suunnittelu- **asetukset** (vaihde)-painiketta.
3.  Valitse **Muokkaa** käynnistääksesi muokkaustilaan työtilassa. **Huomautus:** näkevät kaksi uutta sivua on luotu automaattisesti. Järjestelmä luo nämä sivut, koska on otettu käyttöön tiedostojen hallinta edellisessä jaksossa. Voit ohittaa nämä uudet sivut.
4.  Valitse **Lisää sivulla**.
5.  Kirjoita sivun otsikko, esimerkiksi **Näytä kirjanpidon**, ja kuvaus, kuten **Näytä laskun kirjanpidon**.
6.  Click **Done**.
7.  - **Kentät** -välilehdessä **kentät**, jaot-sivulla Valitse seuraavat kentät ja valitse sitten **tehty**:
    1.  Summa
    2.  Valuutta
    3.  Kirjanpitotili

> [!NOTE] 
> Emme ole valinnut **kuvaus** sarakkeen ruudukon jaot, koska tämän skenaarion vaatimusten vahvistanut, että Laajennettu hinta vain summa, joka on jaot. Tämän vuoksi käyttäjä ei edellyttävät toisen kentän summan tyyppi, joka on jakelu. Kuitenkin seuraava skenaario-olemme **se** käyttää tätä tietoa, koska tämän skenaarion vaatimusten määrittäminen että muuntyyppisiin summan jakelut (kuten arvonlisävero).
8.  Valitse **tehty** Poistu muokkaustilasta.
9.  Valitse **takaisin** ja **tehty** Lopeta työtilan
10. Valitse **julkaista työtilan** tallentaa työsi

**Huomautus:****Näytä kirjanpidon** mobiili sivu ei ole tällä hetkellä linkitetty mobiili-sivut, joita emme ole tähän mennessä suunniteltu. Koska käyttäjä voi siirtyä **Näytä kirjanpidon** sivun **laskun tiedot** sivun mobiililaitteessa, Emme anna Siirtyminen **laskun tiedot** sivulta **Näytä kirjanpidon** sivulla. Voimme vahvistaa tämän siirtymisen muita kautta JavaScript logic.

1.  Avaa .js-tiedosto, jonka loit aiemmin ja lisää seuraava koodi rivit, jotka näkyvät korostettuina. Tämä koodi tekee kaksi asiaa:
    1.  Sen avulla varmistetaan, että käyttäjät ei voi siirtyä suoraan työtilan ja **Näytä kirjanpidon** sivulla.
    2.  Toteaa, että siirtyminen ohjausobjektin **laskun tiedot** sivulta **Näytä kirjanpidon** sivulla.

> [!NOTE] 
> Sivujen ja muiden ohjausobjektien JS-koodin on oltava sama työtilasta.

1.  Tärkein funktio (metadataService, dataService, cacheService, $q) {palauttaa {appInit: funktio (appMetadata) {/ / piilota ohjausobjektit, joiden on oltava läsnä, mutta ei näy metadataService.configureControl (' oma--toimittajalaskujen, 'ShowAccept' {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowApprove' {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowReject', {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowDelegate', {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowRequestChange', {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowRecall' {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowComplete', {piilotettu: TOSI}); metadataService.configureControl (' oma--toimittajalaskujen, 'ShowResubmit' { piilotettu: TOSI}); Piilota sivut ei sovellu root siirtyminen metadataService.hideNavigation('View-accounting'); Linkkiä voit tarkastella kirjanpidon metadataService.addLink ('-laskutustiedot, "View-Kirjanpito ', '-Kirjanpito-nav-Näytönhallinta ',"Näytä kirjanpidon", true); }, pageInit: funktio (pageMetadata, params) {Jos (pageMetadata.Name == "Laskutustiedot") {/ / Näytä/Piilota työnkulkutoimintoja työnkulun perusteella vaihe metadataService.configureAction ('Hyväksy' {näkyvissä: TOSI}); metadataService.configureAction ('Hyväksy' {näkyvissä: TOSI}); metadataService.configureAction (Hylkää, {näkyvissä: TOSI}); metadataService.configureAction ('Edustaja' {näkyvissä: TOSI}); metadataService.configureAction (' pyynnön-muuta ', {näkyvissä: TOSI}); metadataService.configureAction ('Peruuta' {näkyvissä: TOSI}); metadataService.configureAction (kokonais, {näkyvissä: TOSI}); metadataService.configureAction ('Lähetä' {näkyvissä: TOSI});

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

2.  Ladata kooditiedoston työtilaan valitsemalla **logiikan** välilehti, jos haluat korvata aiemman koodin
3.  Valitse **tehty** Poistu muokkaustilasta.
4.  Valitse **takaisin** ja **tehty** Lopeta työtilan
5.  Valitse **julkaista työtilan** tallentaa työsi

### <a name="validation"></a>Valintasäännöt

Kannettavasta laitteesta Avaa sovellus ja muodostamaan yhteyttä Dynamics 365 Operations-esiintymän. Varmista, että kirjaudut yrityksen jossa toimittajalaskuja on määritetty sinulle tarkastelua varten. Olisi voitava suorittaa seuraavat toimet:

-   Katso **Omat hyväksynnät** työtila.
-   Perehtymistä **Omat hyväksynnät** työtilaan ja katso **oma toimittajalaskujen** sivulla.
-   Perehtymistä **oma toimittajalaskujen** sivulle ja haluat tarkastella laskuja, jotka on varattu sinulle.
-   Yksi laskut perehtymistä ja katso laskun otsikkotietojen ja rivin tiedot.
-   Tiedot-sivun linkki liitteet ja tämän linkin avulla voit tarkastella liitteitä ja siirry liitteet luetteloon.
-   Tiedot-sivulla on linkki **tarkastella kirjanpidon** sivulle ja käyttää tätä linkkiä Siirry sivulle jaot ja tarkastella jakoja.
-   Valitse tiedot-sivulla **toiminnot** valikon alaosasta, ja suorittaa työnkulkutoimintoja, joita sovelletaan työnkulun vaiheeseen.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Fabrikam monimutkaisia laskun hyväksynnän Skenaarion suunnitteleminen
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
<td>Laskun otsikon kentät käyttäjä haluavat nähdä mobiili kokemus ja missä järjestyksessä?</td>
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
<td>Laskurivien kenttiä mitä käyttäjän haluat nähdä mobiili kokemus ja missä järjestyksessä?</td>
<td><ol>
<li>Hankintaluokka</li>
<li>Määrä</li>
<li>Yksikköhinta</li>
<li>Rivin nettosumma</li>
<li>Valmisteveron määrä</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kuinka monta laskurivien onko lasku? Käytä tätä 80-20 sääntö ja optimoida 80 prosenttia.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Käyttäjät haluavat tarkastella mobiililaitteen kirjanpidolliset jaot (lasku coding) aikana arvostelut?</td>
<td>Kyllä</td>
</tr>
<tr class="odd">
<td>Kuinka monta kirjanpidolliset jaot (Laajennettu hinta, arvonlisävero, kulut ja niin edelleen) on laskuriviä varten? Käytä uudelleen 80-20 sääntö.</td>
<td>Kokonaishinta: 2 ALV: 2 kulut: 2</td>
</tr>
<tr class="even">
<td>Laskut myös tarvitse kirjanpidollisten jakojen ja laskuotsikon? Jos näin on, nämä kirjanpidolliset jaot on käytettävissä laitteessa?</td>
<td>Ei käytössä</td>
</tr>
<tr class="odd">
<td>Käyttäjät haluavat nähdä laitteen laskulle liitteitä?</td>
<td>Kyllä</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Harjoituksessa

Skenaario 1 Skenaario 2 vaatimukset perustuvat seuraaviin muutoksiin voidaan tehdä. Käyttää käyttö, jotka ovat käytettävissä tämän osan opiskelua varten.

1.  Yksi huoltolaskun rivit odotetaan 2-skenaariossa, koska seuraavat muutokset rakenteeseen auttaa parantaa käyttökokemusta kannettavan laitteen:
    1.  Sen sijaan että tarkastelisit laskurivien tiedot (kuten skenaario 1) sivulla, käyttäjät voivat tarkastella rivejä mobiili erillisellä sivulla.
    2.  Koska tässä tilanteessa on odotettavissa useita laskun rivejä, jos **VendMobileInvoiceAllDistributionTree** -sivua käytetään mobiili (kuten skenaario 1) jaot-sivujen suunnitteluun, se voi olla hämmentävää käyttäjä joka korreloi jaot rivit. Tämän vuoksi käyttää **VendMobileInvoiceLineDistributionTree** sivun jaot sivujen suunnitteluun.
    3.  Parhaassa tapauksessa jakoja voidaan osoittaa laskurivi tässä tilanteessa yhteydessä. Varmista siksi, että käyttäjä voi porautua rivin, voit tarkastella sivun jaot. Sivun linkki-ominaisuuden avulla voit määrittää yksityiskohtaiset tiedot, samalla tavalla kuin skenaario 1 sivujen ylä- ja tiedot.

2.  Useita summatyyppi on odotettavissa, jaot 2-skenaariossa (esimerkiksi arvonlisäveron ja kulut), koska se on näyttää summatyypin kuvaus. (Olemme pois näitä tietoja skenaario 1).

## <a name="conclusion"></a>Johtopäätökset
Mobile platform ja sovelluksen ominaisuuksia avulla voit suunnitella mobiili skenaarioita, jotka on optimoitu käyttäjän organisaation perusta. Jotka ovat tämän ohjeaiheen esimerkkien perusteella, voit yritä muita variaatioita ja luoda erilaisia kokemuksia, jotka vastaavat tiettyjä tarpeita.


