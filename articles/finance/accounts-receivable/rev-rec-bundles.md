---
title: Tuottokirjauksen myyntirakenteet
description: Tässä ohjeaiheessa kuvataan myyntireskontran tuottokirjausominaisuuteen sisältyviä myyntirakennetoimintoja. Myyntirakenne koostuu päänimikkeestä ja useasta komponenttinimikkeestä.
author: kweekley
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 62a4d7f36ad0b36edeaec75e9b670e2aad143703
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725816"
---
# <a name="revenue-recognition-bundles"></a>Tuottokirjauksen myyntirakenteet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan myyntireskontran tuottokirjausominaisuuteen sisältyviä myyntirakennetoimintoja. Myyntirakenne koostuu päänimikkeestä ja useasta komponenttinimikkeestä. Päänimike lisätään myyntitilaukseen, mikä tehostaa tilaustenkäsittelyä. Sen jälkeen se kuitenkin hajotetaan komponenttinimikkeiksi. Komponenttinimikkeet ovat lueteltuina sisäisissä asiakirjoissa, kuten pakkausluettelossa. Ulkoisissa asiakirjoissa näkyy kuitenkin vain päänimike.

> [!NOTE]
> Microsoft Dynamics 365 Commerce -kanavat, kuten online-kanava, myyntipiste (POS) ja puhelinkeskukset, eivät tue tuottokirjausta (eivätkä sen myyntirakennetoimintoja). Tämä koskee myös Dynamics 365 Supply Chain Managementin ja Dynamics 365 Salesin Prospektista käteiseksi ‑ratkaisua. Nimikkeitä, jotka on määritetty käyttämään tuottokirjausta, ei tulisi lisätä tilauksiin tai tapahtumiin, jotka on luotu Commerce-kanavissa tai Prospektista käteiseksi ‑ratkaisussa.

Jotta voit määrittää myyntirakenteita, sinun on syötettävä tuottokirjauksen määritysavaimet. Voit kuitenkin käyttää myyntirakenteita, vaikka tuottokirjausta ei olisi määritetty. Samoin voit käyttää tuottokirjausta, vaikka myyntirakenteita ei olisi määritetty. Jos tuottokirjaus on määritetty, komponenttinimikkeet määrittävät tuottohinnan ja tuottoaikataulun, joita käytetään tuottojen kirjaamiseen tai lykkäykseen, kun myyntitilaus laskutetaan.

Myyntirakenteiden määritys käyttää tuoterakennetoimintoja. Tietoja myyntirakennenimikkeen määrittämisestä on kohdassa [Tuottokirjauksen määritys](revenue-recognition-setup.md). Jos päänimike on merkitty myyntirakenteeksi, sitä käsitellään eri tavalla kuin muita tuoterakennenimikkeitä. Seuraavassa on luettelo eroista:

- Myyntirakenne on hajotettava myyntitilauksen vahvistuksen kautta valitsemalla myyntitilaussivun toimintoruudun **Myynti**-välilehdestä **Vahvista myyntitilaus**. Myyntirakennenimikkeitä ei saa hajottaa valitsemalla **Myyntitilausrivit**-pikavälilehden **Myyntitilausrivi**-valikon **Hajota**-kohdasta **Tuoterakennerivi**. Silloin nimikettä käsiteltäisiin tuoterakenteena eikä myyntirakenteena.
- Myyntitilaus, joka sisältää myyntirakennenimikkeen, on vahvistettava ennen pakkausluettelon tai laskun luomista.
- Kun myyntirakenne hajotetaan myyntitilauksen vahvistuksen kautta, päänimike peruutetaan ja sen yksikköhinta ja alennukset kohdistetaan myyntirakenteen komponenttinimikkeille.
- Komponenttinimikkeiden summan on aina oltava sama kuin päänimikkeen hinta. Tämän vuoksi komponenttinimikkeiden kenttiä voidaan päivittää tai muuttaa vain rajoitetusti. Esimerkiksi yksikköhintaa ei voi muuttaa manuaalisesti. Sitä ei voi muuttaa epäsuorasti saattamalla voimaan uutta hintasopimusta. Uuden hintasopimuksen estämiseksi komponenttinimikkeiden varastodimensioita ei voi muuttaa.
- Kun tulostetaan ulospäin näkyvä asiakirja, kuten myyntitilausvahvistus tai lasku, siihen tulostetaan päänimike komponenttinimikkeiden sijaan.

## <a name="bundles-on-sales-orders"></a>Myyntitilausten myyntirakenteet

USMF-esittely-yritys sisältää seuraavat myyntirakenneasetukset. Huomaa, että kaikki tuottokirjausasetukset, kuten tuottoaikataulujen asetukset, on poistettu tähän skenaarioon sisältyviltä nimikkeiltä.

**Päänimike:** Kannettava tietokone ‑myyntirakenne

- **Komponenttinimike:** määrä 1 kpl nimikettä 1000
- **Komponenttinimike:** määrä 1 kpl nimikettä S0021
- **Komponenttinimike:** määrä 1 kpl nimikettä Tuki

Komponenttinimikkeiden *perusmyyntihinta* on olennainen osa komponenttien asetuksia. Perusmyyntihinta määritetään nimikkeen **Myynti**-pikavälilehdessä. Sitä käytetään kohdistuskertoimen laskemiseen, kun päänimikkeen yksikköhinta kohdistetaan komponenttinimikkeisiin. Kauppasopimuksen myyntihintoja ei koskaan käytetä tähän tarkoitukseen.

Komponenttinimikkeille on määritetty seuraavat perusmyyntihinnat:

- **1000:** 1 900,00 $
- **S0021:** 150,00 $
- **Tuki:** 500,00 $

Myyntitilaus syötetään asiakkaalle US-004, Cave Wholesales. Ainoa syötettävä rivi on Kannettava tietokone ‑myyntirakennenimikkeen rivi. Päärivin oletusyksikköhinta voidaan ottaa useasta eri paikasta, kuten kauppasopimuksesta tai perusmyyntihinnasta. Tässä esimerkissä yksikköhinnaksi syötettiin manuaalisesti 2 300 $.

[![Kannettava tietokone ‑myyntirakennenimike myyntitilauksessa.](./media/bundle-01.png)](./media/bundle-01.png)

Koska myyntitilauksessa on myyntirakenne, se on vahvistettava. Vahvistusvalintaikkunassa näkyvät myyntirakenteen komponentit.

[![Vahvista myyntitilaus ‑valintaikkuna, jossa näkyvät komponenttinimikkeet.](./media/bundle-02.png)](./media/bundle-02.png)

Tulostetussa vahvistusraportissa näkyy kuitenkin vain myyntirakenteen päänimike, koska raportti on ulospäin asiakkaalle näkyvä asiakirja.

[![Vahvistusraportti, jossa näkyy vain päänimike.](./media/bundle-03.png)](./media/bundle-03.png)

Kun myyntitilaus on vahvistettu, päänimike näkyy edelleen myyntitilauksessa, mutta sen tilaksi on muutettu **Peruutettu**. Lisäksi nettosummaa seurataan **Myyntirakenteen nettosumma** ‑kentässä. Tämä summa tarvitaan laskun tulostamiseen, koska laskussa näkyy päänimike, eikä komponenttinimikkeitä.

Komponenttinimikkeiden summan on oltava sama kuin päänimikkeen **Myyntirakenteen nettosumma** ‑arvo, koska tämä arvo on summa, joka näkyy asiakkaalle tulostetussa laskussa. Komponenttinimikkeiden muokkaaminen on rajoitettua, jotta lasku vastaa kirjanpitoon kirjattuja summia. Esimerkiksi toimipaikkaa ja varastoa ei voi muuttaa, koska niiden muuttaminen voisi aiheuttaa kauppasopimuksen perusteella hinnanmuutoksen.

Päänimikkeen rivin yksikköhinta kohdistetaan komponentteihin seuraavasti:

**Komponenttien perusmyyntihinnat yhteensä:** 1 900 $ + 500 $ + 150 $ = 2 550 $

- **Komponentti 1:** 2 300 $ × (1 900 ÷ 2 550) = 1 713,73 $
- **Komponentti 2:** 2 300 $ × (500 ÷ 2 550) = 450,98 $
- **Komponentti 3:** 2 300 $ × (150 ÷ 2 550) = 135,29 $

Komponenttien summan on oltava 2 300 $, kuten se onkin (1 713,73 $ + 450,98 $ + 135,29 $ = 2 300 $).

Jos kaikkiin komponenttinimikkeisiin on tarpeen tehdä muutoksia, päänimike voidaan poistaa. Tässä tapauksessa myös komponenttinimikkeet poistetaan. Päänimike voidaan sitten lisätä uudelleen ja tarvittavat muokkaukset voidaan tehdä, ennen kuin myyntitilaus vahvistetaan.

[![Myyntirakennenimike, joka sisältää komponenttinimikkeiden muutokset.](./media/bundle-04.png)](./media/bundle-04.png)

Kun myyntitilaus kerätään ja pakataan, asiakirjoihin sisältyvät vain myyntirakenteen komponentit. Pakkausluettelon ja laskun on sisällettävä kokonainen myyntirakenne. Muussa tapauksessa niitä ei voi kirjata. Tarkastellaan esimerkkiä, jossa valintaikkunassa näkyy komponenttinimikettä. Jos yrität poistaa yhden niistä, saat virhesanoman, jonka mukaan kaikki myyntirakenteen tuotteet on lähetettävä, ennen kuin ne voidaan laskuttaa.

Myyntirakenne on lähetettävä ja laskutettava kokonaisena myyntirakenteena. Jos muutat esimerkiksi nimikkeen 1000 määräksi 4, mutta muiden komponenttinimikkeiden määräksi jää 5, pakkausluetteloa ja laskua ei voi kirjata.

Osasumman voi lähettää ja laskuttaa vain, jos kaikkien myyntirakenteen komponenttien määrä pienenee. Myyntitilaukseen lisätään esimerkiksi viisi Kannettava tietokone ‑myyntirakennenimikettä. Kun myyntitilaus on vahvistettu, kolme komponenttinimikettä näkyvät myyntitilauksessa ja kunkin niistä määrä on 5. Lähetyksessä ja laskutuksessa kullekin komponentille tulee oletusarvon mukaan määräksi 5. Voit kuitenkin muuttaa kaikkien kolmen komponenttinimikkeen määräksi 3. Tällöin lähetetään ja laskutetaan kolme täyttä myyntirakennetta. Jäljellä olevat kaksi myyntirakennenimikettä (kunkin kolmen komponenttinimikkeen määrä on 2) voidaan lähettää ja laskuttaa myöhemmin.

Viimeinen vaihe on myyntitilauksen laskuttaminen. Laskutuksen aikana laskuvalintaikkunassa näkyvät komponenttinimikkeet.

[![Laskuvalintaikkuna, jossa näkyvät komponenttinimikkeet.](./media/bundle-06.png)](./media/bundle-06.png)

Tulostetussa laskussa näkyy kuitenkin vain päänimike.
 
[![Tulostettu lasku, jossa näkyy vain päänimike.](./media/bundle-07.png)](./media/bundle-07.png)

Kirjauksen jälkeen luotu laskukirjauskansio ei sisällä päänimikettä myyntirakenteesta, koska nimikkeen tila on **Peruutettu**.

[![Laskukirjauskansio, joka ei sisällä päänimikettä.](./media/bundle-08.png)](./media/bundle-08.png)

On tärkeää, ettei laskukirjauskansioon sisällytetä päänimikettä myyntirakenteesta, koska kaikki laskun kirjaamisen jälkeen suoritettavat prosessit perustuvat tähän laskukirjauskansioon. Jos esimerkiksi luot hyvityslaskun toimintoruudun **Myynti**-välilehdessä, luotava hyvityslasku sisältää komponenttinimikkeet, mutta ei päänimikettä.

[![Hyvityslasku, jossa näkyvissä ovat komponenttinimikkeet ilman päänimikettä.](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
