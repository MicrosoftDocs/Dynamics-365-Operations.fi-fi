---
title: Myyntitilauksen kirjaaminen
description: Tässä artikkelissa on tietoja varaston kirjausprofiilisivun Myyntitilaus-välilehdestä.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5ea1c3c90b32d18243615e3ff283e1e818ac23b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886310"
---
# <a name="sales-order-posting"></a>Myyntitilauksen kirjaaminen

**Varastokirjausprofiilit**-sivun **Myyntitilaus**-välilehden avulla voit hallita, miten myyntitilaukset kirjataan kirjanpitoon. Myyntitilauksen kirjanpitoon kirjataan kaksi päätehtävää: 

- Pakkausluettelo
- Lasku

Jotta fyysinen tapahtuma (pakkausluettelo) kirjattaisiin myyntitilauksen pääkirjaan, seuraavien ehtojen on täytyttävä:

- **Varasto ja varastonhallinnan parametrit** -sivulla on valittava **Kirjaa pakkausluettelo kirjanpitoon** -valintaruutu.
- Myyntitilausrivillä valitun nimikkeen **Nimikemalliryhmä**-sivulla on valittava **Kirjaa varastotilanne kirjanpitoon** -valintaruutu.
- **Varastokirjausprofiili**-sivulla on määritettävä päätilit seuraaville kirjaustyypeille:
  - Toimitettujen yksiköiden kustannus
  - Toimitettujen myytyjen tuotteiden kustannukset

Jotta kirjanpitotapahtuma (lasku) kirjattaisiin myyntitilauksen pääkirjaan, seuraavien ehtojen on täytyttävä:

- Myyntitilausrivillä valitun nimikkeen **Nimikemalliryhmä**-sivulla on valittava **Kirjaa kirjanpitovarasto kirjanpitoon** -valintaruutu.
- **Varastokirjausprofiili**-sivulla on määritettävä päätilit seuraaville kirjaustyypeille:
  - Yksiköiden kustannukset – laskutettu
  - Myytyjen tuotteiden kustannukset – laskutettu
  - Myyntituotto
  - Alennus\*

> [!NOTE]
> Alennustili on valinnainen. Monissa kirjanpidon määräyksissä, kuten GAAP- ja IFRS-määräyksissä, edellytetään, että alennukset vähentävät myyntituottoa, joten tilejä ei käytetä useissa tilanteissa. Jos paikalliset säädökset sallivat, käytä erillistä päätiliä alennetun myyntihinnan osan kirjaa varten.

Jotta viivästetty (arvioitu) tulon arvo kirjattaisiin pääkirjaan, kun luot pakkausluettelon myyntitilaukselle, seuraavien ehtojen on täytyttävä:

- Myyntitilausrivillä valitun nimikkeen **Nimikemalliryhmä**-sivulla on valittava **Kirjaa varastotilanne kirjanpitoon** -valintaruutu.
- **Nimikemalliryhmä**-sivulla **Kirjaa lykätyn tuoton tilille myynnin toimituksessa** -valintaruudun on oltava valittuna.
- **Varasto ja varastonhallinnan parametrit** -sivulla on valittava **Kirjaa pakkausluettelo kirjanpitoon** -valintaruutu.
- **Varasto ja varastonhallinnan parametrit** -sivulla on valittava **Kirjaa todellinen arvonlisävero** -valintaruutu.
- **Myyntireskontran parametrit** -sivulla on valittava **Kirjaa pakkausluettelo kirjanpitoon** -valintaruutu.
- **Varastokirjausprofiili**-sivulla on määritettävä päätilit seuraaville kirjaustyypeille:
  - Lykätty tuotto toimituksessa
  - Lykätyn tuoton vastakirjaus toimituksessa
  - Toimituksen lykätty arvonlisävero

> [!NOTE]
> On suositeltavaa ottaa käyttöön **Kirjaa varastotilanne** ja **Kirjaa pakkausluettelo kirjanpitoon**. Näiden asetusten ottaminen käyttöön voi nopeuttaa kuukauden lopun sulkemismenettelyitä, koska lykkäyksiä ei tarvitse laskea ja kirjata manuaalisesti. Lisäksi raportit kuvastavat lykättyjä summia automaattisesti ilman manuaalista väliintuloa.

> [!IMPORTANT]
> **Kirjaa lykätyn tuoton tilille myynnin toimituksessa** -vaihtoehtoa ei käytetä tuottojen kirjaamisen yhteydessä. Lisätietoja tuottojen kirjaamista on kohdassa [Tuottokirjausten yleiskatsaus](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>Malli kirjausprofiilin konfiguraatiosta 

Seuraavassa taulukossa on esimerkkejä oletuskirjaustyypeistä sekä esimerkkejä päätileistä ja kuvauksista:
 
- **Selvitystili**-sarake ilmaisee, että kirjaustyyppi on selvitystili. Tälle tilille kirjattu summa palautetaan automaattisesti, kun myöhempi tapahtuma kirjataan. 
- **P/F**-sarakkeessa näkyy **P** fyysistä kirjausta varten ja **F** taloushallinnon kirjausta varten. 
- **Seuraa**-sarakkeessa näkyy, onko tietyn kirjaustyypin päätili tavallisesti sama kuin toinen kirjaustyyppi. Sarakkeen arvo ilmaisee yleensä käytetyn kirjaustyypin.

> [!NOTE]
> Nämä päätilit ja päätilien nimet ovat vain ehdotuksia. Suosittelemme, että määrität yrityksesi tarpeille parhaan konfiguraation yhdessä kirjanpitäjän kanssa.


| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | P/F | Seuraa | Kuvaus |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Toimitettujen yksiköiden kustannus | 140100</br>140101 | Materiaalivarasto</br>Lähetetyt, laskuttamattomat materiaalit | Resurssi | Hyvitys | Kyllä | P | Yksiköiden kustannukset – laskutettu | Käytetään, kun myyntitilauksen pakkausluettelo kirjataan. Tilin vastatili on myytyjen ja toimitettujen tuotteiden kustannukset. Tämän tilin summa peruutetaan, kun myyntitilauslasku kirjataan. Voit käyttää fyysisen varaston tunnuksena Lähetetyt, laskuttamattomat materiaalit -tiliä ja varata materiaalivarastotilin taloudellista päivitystä varten. |
| Toimitettujen myytyjen tuotteiden kustannukset | 500150 | Lykätty MTKUST | Kulut | Veloitus | Kyllä | P  | Käytetään, kun myyntitilauksen pakkausluettelo kirjataan. Tilin vastatili on toimitettujen yksikköjen kustannukset. Tämän tilin summa peruutetaan, kun myyntitilauslasku kirjataan. |
| Yksiköiden kustannukset – laskutettu | 140100 | Materiaalivarasto | Resurssi | Hyvitys | En | F | Toimitettujen yksiköiden kustannus | Käytetään, kun myyntitilauksen lasku kirjataan. Tilin vastatili on myytyjen ja laskutettujen tuotteiden kustannukset. Tämä tili edustaa taseen varastoa. |
| Myytyjen tuotteiden kustannukset – laskutettu | 500100 | MTKUST Materiaalit | Kulut | Veloitus | En | F  | Käytetään, kun myyntitilauksen lasku kirjataan. Tilin vastatili on laskutettujen yksiköiden kustannukset. Tämä tili edustaa MTKUST-kohtaa P&amp;L-lausekkeessa. |
| Tuotto (Myyntitilauksen tuotto*) | 400100 | Tuoton materiaalit | Myyntituotto | Hyvitys | En | F   | Käytetään, kun myyntitilauksen lasku kirjataan. Tämän tilin vastatili on Reskontratili (Asiakkaan saldo*) **Myyntireskontran kirjausprofiilissa**. |
| Provisio (myynti, provisio*) | 602150 | Provisiokulu | Kulut | Veloitus | En | F  | Käytetään, kun provisio on käytössä ja lasketaan myynnistä ja kirjataan myyntitilauslaskuprosessin aikana. Tämän tilin vastatili on maksettava provisio. |
| Provision vastakirjaus (Myynti, provision vastakirjaus*) | 201110 | Maksettavat palkkiot | Velat | Hyvitys | Kyllä | F | Käytetään, kun provisio on käytössä ja lasketaan myynnistä ja kirjataan myyntitilauslaskuprosessin aikana. Tämän tilin vastatili on Provisiokulu. |
| Lykätty tuotto toimituksessa (myynti – pakkausluettelon tuotto*) | 401400 | Jaksotettu myynti | Myyntituotto | Hyvitys | Kyllä | P  | Käytetään, kun lykätty toimitustuotto on käytössä ja kirjataan, kun käsittelet myyntitilauksen pakkausluetteloa. Tämän tilin vastatili on Lykätyn tuoton vastakirjaus. Tämän tilin summat palautetaan automaattisesti myyntitilauslaskua kirjattaessa. |
| Lykätyn tuoton vastakirjaus toimituksessa (myynti – pakkausluettelon tuoton vastaukirjaus)* | 130400 | Myyntireskontra – laskuttamaton | Resurssi | Veloitus | Kyllä | P  | Käytetään, kun lykätty toimitustuotto on käytössä ja kirjataan, kun käsittelet myyntitilauksen pakkausluetteloa. Tämän tilin vastatili on Lykätty tuotto toimituksessa. Tämän tilin summat palautetaan automaattisesti myyntitilauslaskua kirjattaessa. |
| Toimituksen lykätty arvonlisävero (myynti – pakkausluettelon vero*) | 250500 | Lykätty arvonlisävero | Velat | Hyvitys | Kyllä | P  | Käytetään, kun lykätty toimitustuotto on käytössä ja todellisen arvonlisäveron kirjaaminen on otettu käyttöön. Veron summa kirjataan, kun käsittelet myyntitilauksen pakkausluetteloa. |

\*Tämän taulun sulkeissa näkyvät arvot edustavat arvoa, jota käytetään **Tositetapahtumat**-sivun **Kirjaamistyyppi**-kentässä. Voit tarkastella **kirjaustyyppiä** **Tositetapahtumat**-sivun **Yleiset**-välilehdessä.

## <a name="sales-category-posting"></a>Myyntiluokan kirjaus

Vaihtoehtona varastokirjauksen määrittämiselle kaikille nimikkeille, tuoteryhmälle tai yksittäiselle nimikkeelle voit määrittää luokkia ja hallita kirjanpitoa myyntiluokkien mukaan. Lisätietoja luokkahierarkian määrittämisestä ja luokkien määrittämisestä tuotteille on kohdassa [Tuotteiden luokitteluhierarkian luominen](/supply-chain/pim/tasks/create-hierarchy-product-classification.md) ja [Tuotteen luokittelu luokkahierarkioiden avulla](/supply-chain/pim/tasks/classify-product-category-hierarchies.md).

Kun olet luonut luokkahierarkian, sinun on määritettävä hierarkia vähintään yhteen tyyppiin. Jos haluat käyttää myyntitilausten luokkahierarkiaa, sinun on määritettävä luokka myyntiluokkahierarkian tyyppiin. Lisätietoja on kohdassa [Tietoja luokkahierarkioista](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>Luo tulojen kirjaus myyntiluokkien mukaan

Voit määrittää myyntitilaukselle myyntikategorian perusteella kirjanpitokirjauksia seuraavasti:

1. Siirry kohtaan **Varastonhallinta** > **Määritys** > **Kirjaus** > **Kirjaus**.
2. Valitse **Myynti**-välilehti.
3. Valitse määritettävän kirjaustyypin valintapainike (esimerkiksi **Tuotto**).
4. Valitse **Uusi**.
5. Valitse **Nimikekoodi**-kentästä **Luokka**.
6. Valitse **Luokkasuhde**-kentässä kirjausprofiilin luokka.
7. Valitse **Tilikoodi**-kentästä vaihtoehto kohteille **Taulukko**, **Ryhmä** tai **Kaikki**. Jos haluat käyttää kirjausprofiilia esimerkiksi kaikille asiakkaille, valitse **Kaikki**.
   - Jos valitsit vaiheessa 6 **Taulukko**, valitse kirjausprofiilin **toimittajanumero** **Tilisuhde**-kentästä.
   - Jos valitsit vaiheessa 6 **Ryhmä**, valitse kirjausprofiilin **toimittajaryhmä** **Tilisuhde**-kentästä.
   - Jos valitsit vaiheessa 6 **Kaikki**, **Tilisuhde**-kenttä jätetään tyhjäksi.

8. Liitä valittuun kirjaustapaan tietty veroryhmä valitsemalla **Arvonlisäveroryhmä**. Jos jätät tämän kentän tyhjäksi, kirjaustyyppi koskee kaikki veroryhmiä. Veroryhmille määritetty kirjaus koskee vain myynti- ja ostotapahtumia.

9. Määritä **Päätili**-kentässä tilinumero, jolle tilityyppi kirjataan. Valitse yksi tilikartan tilinumeroista.
