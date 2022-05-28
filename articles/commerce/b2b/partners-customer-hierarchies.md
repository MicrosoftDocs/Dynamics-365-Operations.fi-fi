---
title: B2B-liikekumppaneiden hallinta asiakashierarkioiden avulla
description: Tässä aiheessa kuvataan, miten asiakashierarkioita käytetään liikekumppaneiden hallitsemiseen Microsoft Dynamics 365 Commercen yritysten välisten (B2B) verkkokauppasivustojen osalta.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 70acdf469be2fcddd9e2bf755e958c1b20ee2fcf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686568"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>B2B-liikekumppaneiden hallinta asiakashierarkioiden avulla

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten asiakashierarkioita käytetään liikekumppaneiden hallitsemiseen Microsoft Dynamics 365 Commercen yritysten välisten (B2B) verkkokauppasivustojen osalta.

Commerce headquarters -sovelluksessa käytetään *asiakashierarkia*-entiteettiä edustamaan liikekumppaniorganisaatioita, jotka tulevat käyttämään B2B-verkkokauppasivustoasi. Ennen kuin voit alkaa käyttää asiakashierarkioita liikekumppanien hallitsemiseen, sinun on otettava B2B-verkkokauppaominaisuudet käyttöön Commerce headquarters -sovelluksessa ja sitten määritettävä asiakashierarkialle numerosarja.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>B2B-verkkokauppatoiminnon käyttöönotto Commerce headquarters -sovelluksessa

B2B-verkkokauppaominaisuuksien käyttämistä varten on ensin otettava käyttöön **Salli B2B-verkkokauppaominaisuuksien käyttö** -toiminto Commerce headquarters -sovelluksessa.

1. Valitse **Työtilat \> Ominaisuuden hallinta**.
1. Tee **Kaikki**-välilehdessä suodatinruudun avulla haku **Moduuli: Retail ja Commerce**.
1. Etsi toiminto, jonka nimi on **Ota käyttöön B2B-verkkokauppaominaisuudet**, valitse se ja valitse sitten **Ota käyttöön nyt** oikeasta alakulmasta.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Asiakashierarkian numerosarjan määrittämiseen

Numerosarjoilla luodaan luettavia, yksilöllisiä tunnisteita niitä edellyttäville päätietojen tietueille ja tapahtumatietueille. Sinun on määritettävä numerosarja, jota käytetään asiakashierarkian tunnuksen luomiseen. Lisätietoja numerosarjoista on kohdassa [Numerosarjojen yleiskatsaus](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Voit määrittää asiakashierarkian numerosarjan Commerce headquarters -sovelluksessa seuraavien ohjeiden perusteella.

1. Siirry kohtaan **Retail ja Commerce \> Headquartersin asetukset \> Numerosarjat \> Numerosarjat**.
1. Luo uusi numerosarja tai valitse aiemmin luotu numerosarja uudelleen käytettäväksi.
1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan jaetut parametrit**.
1. Lisää **Numerosarjat**-välilehdessä aiemmin luomasi tai valitsemasi numerosarja ja **Asiakashierarkiatunnus**-viitteeseen.

![Numerosarja on lisätty asiakashierarkiatunnus-viitteeseen.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Hyväksyntäprosessin toiminta

Kun liikekumppani pyytää lupaa liittyä B2B-verkkokauppasivustolle, järjestelmä tallentaa pyynnön *prospektina*. Commerce headquarters -sovelluksen henkilötyyppi, kuten vähittäismyynnin toiminnoista vastaavan johtaja, voi hyväksyä tai hylätä kumppanipyyntöjä. Lisätietoja liikekumppanipyyntöjen ja prospektinhyväksyntöjen hallinnasta: [Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa](manage-b2b-users.md).

Kun prospekti hyväksytään, järjestelmä luo kaksi uutta asiakastietuetta:

- Yhden **Organisaatio**-tyypin tietueen edustamaan organisaatiota, joka pyytää liikekumppaniksi hyväksymistä.
- Yhden **Henkilö**-tyypin edustamaan pyynnön lähettänyttä henkilöä.

Lisäksi kohdassa **Retail ja Commerce \> Asiakkaat \> Asiakashierarkia** luodaan uusi asiakashierarkiatietue. Asiakashierarkiatietueella on seuraavat ominaisuudet:

- **Asiakashierarkian tunnus** – Asiakashierarkian yksilöivä tunnus. Tämä tunnus käyttää Commerce headquarters -parametreissa määritettyä numerosarjaa.
- **Nimi** – Liikekumppanin organisaationimi, joka on määritetty rekisteröintipyynnössä. Tämä kenttä on muokattavissa.
- **Tarkoitus** – Tämä ominaisuus on määritetty ennalta määritetylle arvolle **B2B-organisaatio**.
- **Organisaatio** – Liikekumppanin organisaation asiakastunnus.

Käyttöönottopyynnön lähettänyt henkilö lisätään **Hierarkia**-pikavälilehdelle ja hänelle määritetään **Järjestelmänvalvoja**-rooli. Kun järjestelmänvalvoja lisää käyttäjiä B2B-sivuston liikekumppaniorganisaatioon, kullekin käyttäjälle luodaan uusi asiakastietue. Asiakastietue lisätään myös liikekumppanin asiakashierarkiatietueeseen, ja sille määritetään rooli **Käyttäjä**.

### <a name="examples"></a>Esimerkkejä

Sam J -niminen henkilö lähettää käyttöönottopyynnön Microsoft-organisaation puolesta. Kun pyyntö on hyväksytty, luodaan kaksi uutta asiakastiliä: yksi **Henkilö**-tyypin tili Sam J:lle ja yksi **Organisaatio**-tyypin tili Microsoftille.

Kuten seuraavan kuvan esimerkistä näkyy, luodaan myös uusi asiakashierarkiatietue. Tietueella on sama nimi kuin organisaatiolla (**Microsoft**) ja **Järjestelmävalvoja**-rooli on määritetty Sam J:lle. Järjestelmänvalvojana Sam J lisää mahdolliset muut Microsoftin B2B-verkkosivuston käyttäjät tähän hierarkiaan ja määrittää heille **Käyttäjä**-roolin. Tässä esimerkissä Sush R on lisätty käyttäjäksi.

![Esimerkki asiakashierarkiatietueesta.](../media/CustomerHierarchy2.png)

Avaamalla asiakastietueen voit selvittää, onko tietty asiakas liitetty asiakashierarkiaan. Kuten seuraavan kuvan esimerkistä ilmenee **Vähittäismyynti**-pikavälilehden **B2B**-osan **Asiakashierarkia**-kentässä näkyy, kuuluuko asiakas asiakashierarkiaan ja **B2B-järjestelmänvalvoja**-asetus ilmaisee, onko asiakas kyseisen hierarkian järjestelmänvalvoja.

![Esimerkki asiakastietueen Vähittäismyynti-pikavälilehden B2B-osasta, jossa asiakas on liitetty hierarkiaan ja määritetty järjestelmänvalvojaksi.](../media/CustomerHierarchyMapping2.png)

Useimmissa tapauksissa hierarkian kaikkien asiakastietueiden ominaisuuksien arvojen pitäisi vastata toisiaan. Esimerkiksi koska kaikkien liikekumppanien käyttäjien tulisi saada samanlaisia hintoja tuotteille, hintaryhmän ja siihen liittyvien konfiguraatioiden tulisi täsmätä. Järjestelmä ei kuitenkaan pakota tämän yhdenmukaisuuden noudattamista. Siksi relevantit Commerce headquarters -käyttäjät ovat vastuussa siitä, että ominaisuusarvot ja konfiguroinnit vastaavat toisiaan annetun hierarkian kaikille asiakkaille.

Commerce headquarters -käyttäjät voivat tarkastella hierarkian kaikkien asiakastietueiden ominaisuusarvoja vierekkäisessä näkymässä. Kuten seuraavan kuvan esimerkistä ilmenee, voit käyttää **Hierarkia**-pikavälilehden avattavan luettelon **Yleistä**-asetusta ja valita sitten minkä tahansa asiakastietueen osan tarkastellaksesi siihen liittyviä ominaisuuksia. Käyttäjät voivat muokata ominaisuusarvoja suoraan tässä näkymässä. Voit kopioida kaikki järjestelmänvalvoja-asiakastietueen arvot kaikille käyttäjille valitsemalla **Hierarkia**-pikavälilehdessä **Ohita**.

![Esimerkki asiakashierarkiatietueesta, jossa näkyvät Ohita-painike ja avattavan luettelon asetus.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
