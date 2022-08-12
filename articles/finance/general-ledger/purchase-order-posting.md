---
title: Ostotilauksen kirjaus
description: Tässä artikkelissa kuvaillaan varastokirjausprofiilit-sivun ostotilausvälilehti.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 38a9e2740232b18255109ba867fcdddd5b890774
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151029"
---
# <a name="purchase-order-posting"></a>Ostotilauksen kirjaus

**Varastokirjausprofiilit**-sivun **Ostotilaus**-välilehden avulla voit hallita, miten ostotilaukset kirjataan kirjanpitoon. Ostotilauksen kirjanpitoon kirjataan kaksi päätehtävää: 

- Tuotteen vastaanotto
- Lasku

Jotta fyysinen tapahtuma (tuoteluettelo) kirjattaisiin ostotilauksen pääkirjaan, seuraavat valintaruudut on valittava:

- **Varasto ja varastonhallinnan parametrit** -sivulla on valittava **Kirjaa vastaanotto kirjanpitoon** -valintaruutu.
- **Kirjaa varastotilanne**- ja **Jaksota ostovelka tuotteen vastaanotossa** -valintaruudut **Nimikemalliryhmät**-sivulla.

**Varastokirjausprofiili**-sivulla on määritettävä päätilit seuraaville kirjaustyypeille:

- Vastaanotettujen laskutettujen ostettujen materiaalien kustannus
- Ostomeno, laskuttamaton
- Osto, jaksotus

Jotta kirjanpitotapahtuma (lasku) kirjattaisiin ostotilauksen pääkirjaan, seuraavien ehtojen on täytyttävä:

- **Kirjaa kirjanpitovarasto** -valintaruutu on valittava **Nimikemalliryhmät**-sivulla ostotilausrivillä valitulle nimikkeelle.
- **Varastokirjausprofiili**-sivulla on määritettävä päätilit seuraaville kirjaustyypeille:
  - Laskutettujen ostettujen materiaalien kustannus
  - Tuotteen ostomeno
  - Osto, kulu
  - Alennus (valinnainen)

## <a name="fixed-receipt-price-posting"></a>Kiinteän vastaanottohinnan kirjaus

Voit käyttää kiinteää vastaanottohintaa vakiokustannuksena tuotteelle vaihtoehtona sille, että valitset nimikkeelle **Standardikustannus**-vaihtoehdon **Varastomalli**-kentässä **Nimikemalliryhmät**-sivulla. Pääasiallinen ero on se, että kun käytetään **kiinteää vastaanottohintaa**, nimikkeelle käytetään nykyistä kustannushintaa, kun vastaanotto kirjataan. **Kiinteälle vastaanottohinnalle** ei ole uudelleenarvostusprosessia; kun kirjanpidollinen päivitys kirjataan, nykyistä kustannushintaa käytetään kirjaushetkellä. Jos vastaanoton ja laskun kustannushinnan välillä on ero, varianssi kirjataan kiinteän vastaanottohinnan tulostileille.

Jos haluat käyttää tuotteen kiinteää vastaanottohintaa, sinun on tehtävä seuraavat määritykset:

- Valitse **Nimikemalliryhmät**-sivulla **Kirjaa varastotilanne**- ja **Kiinteä vastaanottohinta** -valintaruudut. 
- Valitse **Varasto ja varastonhallinnan parametrit** -sivulla **Kirjaa pakkausluettelo kirjanpitoon** -valintaruutu.
- Määritä **Varastokirjausprofiili**-sivulla päätilit seuraaville kirjaustyypeille:
  - Kiinteän vastaanottohinnan voitto
  - Kiinteän vastaanottohinnan tappio
  - Kiinteän vastaanottohinnan vastakirjaus

Lisätietoja: [Kiinteä vastaanottohinta](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="purchase-charges-and-stock-variation-posting"></a>Oston kulut ja varastomuutoksen kirjaus

Jos aiot ottaa huomioon ostokulut ja varastomuutokset, toimi seuraavasti:

- Valitse **Ostoreskontran parametrit** -sivun **Lasku**-välilehdessä **Kirjaa kirjanpidon veloitustilille** -valintaruutu.
- Valitse ostotilausrivillä valitun nimikkeen **Nimikemalliryhmät**-sivulla **Kirjaa varastotilanne**-, **Kirjaa kirjanpitovarasto**- ja **Jaksota ostovelka tuotteen vastaanotossa** -valintaruudut.
- Valitse **Hankintaparametrit**-sivulla **Luo veloitukset tuotteen vastaanottoon** -valintaruutu.
- Valitse **Varasto ja varastonhallinnan parametrit** -sivulla **Kirjaa pakkausluettelo kirjanpitoon** -valintaruutu.

**Varastokirjausprofiili**-sivulla on määritettävä päätilit seuraaville kirjaustyypeille:

- Ostomeno, laskuttamaton
- Tuotteen ostomeno
- Varastomuutos

> [!NOTE]
> **Veloitus**-kirjaustyyppiä ei käytetä, kun **Kirjaa kirjanpidon veloitustilille** -parametri on valittu.

Lisätietoja: [Kirjaa kirjanpidon periaatteen veloitustilille](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md).

## <a name="sample-posting-profile-configuration"></a>Malli kirjausprofiilin konfiguraatiosta

Seuraavassa taulukossa on esimerkkejä oletuskirjaustyypeistä sekä esimerkkejä päätileistä ja kuvauksista:

- **Selvitystili**-sarake ilmaisee, että kirjaustyyppi on selvitystili. Tälle tilille kirjattu summa palautetaan automaattisesti, kun myöhempi tapahtuma kirjataan. 
- **P/F**-sarakkeessa näkyy **P** fyysistä kirjausta varten ja **F** taloushallinnon kirjausta varten. 
- **Seuraa**-sarakkeessa näkyy, onko tietyn kirjaustyypin päätili tavallisesti sama kuin toinen kirjaustyyppi. Sarakkeen arvo ilmaisee yleensä käytetyn kirjaustyypin.

> [!NOTE]
> Päätilit ja päätilien nimet ovat vain ehdotuksia. Suosittelemme<!--note from editor: Via Writing Style Guide.--> että määrität yrityksesi tarpeille parhaan konfiguraation yhdessä kirjanpitäjän kanssa.


| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | P/F | Seuraa | Kuvaus |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Vastaanotettujen laskutettujen ostettujen materiaalien kustannus | 140100</br>140101 | Materiaalivarasto</br>Lähetetyt, laskuttamattomat materiaalit | Resurssi | Veloitus | Kyllä | P | Laskutettujen ostettujen materiaalien kustannus | Käytetään, kun ostotilauksen tuotevastaanottoa kirjatessa vastatili on Ostomeno, laskuttamaton. Tämän tilin summa peruutetaan, kun ostotilauslasku kirjataan. |
| Ostomeno, laskuttamaton | 600180 | Materiaalivastaanotot | Kulut | Veloitus | Kyllä | P | |Käytetään, kun ostotilauksen tuotevastaanotto kirjataan. Vastaanottoon luodaan kaksi tositetta, joita käytetään ostohinnan varianssin seuraamiseen, kun vakiokustannusta käytetään. Ensimmäisen tositteen tilin vastatili on Osto, jaksotus. Toisen tositteen tilin vastatili on Vastaanotettujen laskutettujen ostettujen materiaalien kustannus- ja Ostohintavarianssi-tilien summa. Tälle tilille kirjatut summat peruutetaan, kun ostotilauslasku kirjataan. |
| Laskutettujen ostettujen materiaalien kustannus | 140100 | Materiaalivarasto | Resurssi | Veloitus | En | F  |Vastaanotettujen laskutettujen ostettujen materiaalien kustannus | Käytetään, kun ostotilauksen lasku kirjataan. Tämän tilin vastatili on Tuotteen ostomeno. Tämä tili edustaa taseen varastoa. Käytetty tili on tavallisesti sama tili, jota käytetään myyntitilaukselle (Toimitettujen yksiköiden kustannus ja Yksiköiden kustannukset – laskutettu). |
| Tuotteen ostomeno | 600180 | Materiaalivastaanotto | Kulut | Hyvitys | Kyllä | F  | |Käytetään, kun ostotilauksen lasku kirjataan. Laskuun luodaan kaksi tositetta, joita käytetään ostohinnan varianssin seuraamiseen, kun vakiokustannusta käytetään. Tämän tilin vastatili on Ostomeno, laskuttamaton -tili, jota käytetään vastaanoton kirjauksessa ja palautuksessa laskun kirjauksen aikana. Ilmaisee laskutuksessa ostetun varaston kustannukset, jotka eivät näy taseen varastotilillä. Tämä ostohintavarianssin tuloksen kirjaus nähdään useimmin standardikustannusnimikkeiden ostoissa.|
| Kiinteän vastaanottohinnan voitto (Osto, kiinteän vastaanottohinnan voitto*) | 510310 | Ostohintavarianssi | Kulut | Hyvitys | En | F | Kiinteän vastaanottohinnan tappio | Käytetään, kun ostotilauslasku on kirjattu ja laskutetun hinnan ja nimikkeen oletuskustannuksen välillä on ero. Tätä tiliä käytetään, kun ero on suurempi. Tämän tilin vastatili on Kiinteän vastaanottohinnan vastakirjaus. |
| Kiinteän vastaanottohinnan tappio (Osto, kiinteän vastaanottohinnan tappio*) | 510310 | Ostohintavarianssi | Kulut | Veloitus | En | F | Kiinteän vastaanottohinnan voitto | Käytetään, kun ostotilauslasku on kirjattu ja laskutetun hinnan ja nimikkeen oletuskustannuksen välillä on ero. Tätä tiliä käytetään, kun ero on pienempi. Tämän tilin vastatili on Kiinteän vastaanottohinnan vastakirjaus. |
| Kiinteän vastaanottohinnan vastakirjaus (Osto, kiinteän vastaanottohinnan vastakirjaus*) | 140900 | Varastomuutos | Resurssi | Molemmat | En | F  | |Käytetään, kun ostotilauslasku on kirjattu ja laskutetun hinnan ja nimikkeen oletuskustannuksen välillä on ero. Tämän tilin vastatilit ovat Kiinteän vastaanottohinnan tulostilit. |
| Kulu | Ei saatavilla | Ei saatavilla | Ei saatavilla | Ei saatavilla | Ei saatavilla | Ei saatavilla | Ei saatavilla | Tätä tiliä ei enää käytetä. Käytä sen sijaan Varastomuutoksia. |
| Varastomuutos | 600170 | Varastomuutos | Kulut | Hyvitys | En | Molemmat | | Tätä tiliä käytetään, kun: <ul><li>Tuotteen vastaanoton ja laskun yksikköhinnan välillä on ero.</li><li>Kulut kirjataan nimikkeeseen.</li><li>Epäsuorat kustannukset on<!--note from editor: Edit okay?--> lisätty ostettuihin nimikkeisiin. </li><li>Tämän tilin vastatili on Ostomeno, laskuttamaton.</li></ul> |
| Osto, jaksotus | 200140 | Jaksotetut ostot | Velat | Hyvitys | Y | P | |Käytetään, kun ostotilauksen tuotevastaanotto kirjataan ja ostomäärien jaksotusvaihtoehto on otettu käyttöön. |
| Arvonlisäveron kertymä vastaanotossa | 250500 | Jaksotettu arvonlisävero | Velat | Hyvitys | Y | Molemmat  | |Tätä tiliä käytetään, kun olet valinnut **Kirjaa fyysinen vero** -vaihtoehdon **Varasto ja varastonhallinnan parametrit** -kohdassa ja sinulla on verollinen ostotilaus. Summa kirjataan, kun ostotilaus päivitetään fyysisesti (tuotteen vastaanotto) ja palautetaan, kun ostotilaus kirjataan kirjanpitoon (lasku). |
| Käyttöomaisuuden vastaanotto (käyttöomaisuuden veloitus*) | 180100 | Aineelliset käyttöomaisuuserät | Resurssi | Veloitus | N | Molemmat | Molemmat | Tätä tiliä käytetään, kun vaihtoehto valitaan käyttöomaisuuserien ostotilausrivillä. Ostotilauksen integrointi on määritetty hankkimaan käyttöomaisuuserä tuotteen vastaanoton tai laskun yhteydessä. Lisätietoja käyttöomaisuuden ostotilauksen integroinnista: [Käyttöomaisuuserien hankinta](/fixed-assets/acquire-assets-procurement). |
| Osto, kulu | 618900 | Muu kulu | Kulut | Veloitus | N | Molemmat | |Käytetään kirjattaessa tuotevastaanottoa tai laskua ostotilaukselle, kun nimikkeitä ei ole varastossa, tai kun käytetään hankintaluokkaa. |
| Ennakkomaksu | 132190 | Ennalta maksettu kulu | Resurssi | Veloitus | N | Molemmat | | Käytetään käsiteltäessä ostotilauksen ennakkomaksulaskua. |


\*Sulkeissa näkyvät arvot ilmaisevat arvon, jota käytetään **Tositetapahtumat**-sivun **Kirjaamistyyppi**-kentässä. Voit tarkastella **kirjaustyyppiä** **Tositetapahtumat**-sivun **Yleiset**-välilehdessä.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Käyttöomaisuuden kirjaus ostotilauksilla

Jos käytät **Käyttöomaisuus**-moduulia ja suunnittelet käyttöomaisuuden ostamista ostotilausten avulla, sinun on määritettävä **Käyttöomaisuuden vastaanotto** -kirjaustyyppi **Ostotilaus**-välilehdessä **Varastokirjausprofiili**-sivulla. Lisätietoja: [Käyttöomaisuuden integrointi](/fixed-assets/fixed-asset-integration.md) ja [Käyttöomaisuuserien luominen ja hankkiminen ostoreskontrasta](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Ennakkomaksua edellyttävän ostotilauksen laskun kirjaus

Jos aiot käyttää **Ennakkomaksulasku**-ominaisuutta ostotilauksille, **Ennakkomaksu**-kirjaustyyppi on valittava **Ostotilaus**-välilehdessä **Varaston kirjausprofiili** -sivulla. Lisätietoja: [Ennakkomaksulaskujen ja ennakkomaksujen vertailu](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Ostoehdotuksen ja ostotilauksen vahvistuksen kirjaus

Ostoehdotukset ja ostotilausvahvistukset voi myös konfiguroida niin, että ne kirjaavat alustavat varaukset ja varaukset kirjanpitoon. Kirjausten hallinnassa käytetään kirjausmääritystä. Lisätietoja on kohdassa [Tietoja tilausnumeroiden varauksista](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Tuotteiden hankintaluettelon kirjaukset

Vaihtoehtona varastokirjauksen määrittämiselle kaikille nimikkeille, tuoteryhmälle tai yksittäiselle nimikkeelle voit määrittää luokkia ja hallita kirjanpitoa hankintaluokkien mukaan. Jos haluat lisätietoja luokkien määrittämisestä ja niiden delegoimisesta tuotteille, siirry tämän artikkelin aikaisempaan kohtaan [Malli kirjausprofiilin konfiguraatiosta](#sample-posting-profile-configuration).

Kun luokkia käytetään ostotilausten ja toimittajalaskujen yhteydessä, luokkahierarkia on määritettävä **Hankintaluokkahierarkia**-tyypille **Luokkahierarkian roolin määritykset** -sivulla.

### <a name="vendor-invoices-with-procurement-categories"></a>Toimittajalaskut ja hankintaluokat

Jos organisaatiossa käytetään ostotilauksia joihinkin ostoihin, voit käsitellä ostotilauksiin ei-liittyviä laskuja monella tavalla. Tähän kuuluu kirjauskansioiden käyttö **ostoreskontrassa** tai **Odottavat toimittajan laskut** -sivulla, jota käytetään laskujen muodostamiseen ostotilauksille. Kun luot laskuja, jotka eivät liity ostotilauksen laskuihin, sinun on luotava hankintaluokat kullekin kulutyypille. Sinun on liitettävä luokka oikeaan kulutiliin **Varaston kirjausprofiilit** -sivulla.

Luokkien tarkka määrä vaihtelee laskujen kirjaamiseen käytettävän kulutilien määrän mukaan. Tarvitset vähintään yhden hankintaluokan kullekin päätilille, jota käytät ostotilauslaskuihin liittymättömien laskujen kulutiliveloittamiseen. Yhtä päätiliä varten voidaan käyttää useita luokkia. Tästä voi olla hyötyä käyttämiäsi kulutyyppejä käytettäessä, haettaessa ja raportoitaessa.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Toimittajan laskujen hankintaluokkien käytön edut

Toimittajan laskujen hankintaluokkien käytön etuihin kuuluvat:

- Yhdenmukainen käyttäjäkokemus: Kun määrität hankintaluokkia kaikille ostotilauksiin liittymättömille kuluille, käyttäjille voi opettaa yhden laskutusprosessin käyttämällä **Odottavat toimittajan laskut** -sivua.
- Parannetut raportointikokemukset: Kun määrität hankintaluokkia kaikille nimikkeille ja kaikille ostotilauksiin liittymättömille kuluille, hankinnan kulutusraportti analysoi kulutuksen esimerkiksi toimittajan ja luokan mukaan.
- Yhdenmukainen työnkulku: Kun käytät **Odottavia toimittajan laskuja** kaikkien laskujen käsittelyä varten, voit luoda yhdenmukaisen työnkulun ja hyväksyntäprosessin käyttämällä vain yhtä työnkulkua.

## <a name="consignment-inventory-posting"></a>Tavaralähetysvaraston kirjaus

Tavaralähetysvarastossa käytetään samaa kirjanpidon kirjausta kuin muissa ostetuissa nimikkeissä. Erona on se, että kun varasto vastaanotetaan, kirjanpitotapahtumia ei kirjata. Omistajuuden siirtämiseksi, kun **Varaston omistajuuden muutos** -kirjauskansio on kirjattu, muodostetaan tosite, joka kirjaa nimikkeen kustannukset. Lisätietoja on kohdassa [Tavaralähetyksen määrittäminen](/supply-chain/inventory/consignment.md).
