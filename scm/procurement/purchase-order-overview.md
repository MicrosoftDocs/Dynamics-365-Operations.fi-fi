---
title: Ostotilausten yleiskatsaus
description: "Tässä artikkelissa on yleisiä tietoja ostotilauksista ja linkkejä muita ostotilauksen eri vaiheita käsitteleviin artikkeleihin."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: aed1a411aaefeebb96c2b922afc2e3e7f82cdbb7
ms.lasthandoff: 03/31/2017


---

# <a name="purchase-order-overview"></a>Ostotilausten yleiskatsaus

Tässä artikkelissa on yleisiä tietoja ostotilauksista ja linkkejä muita ostotilauksen eri vaiheita käsitteleviin artikkeleihin.

Ostotilaus on asiakirja, joka ilmaisee toimittajan kanssa tehdyn sopimuksen hyödykkeiden tai palvelujen ostamisesta. Asiakirjan avulla voi myös seurata tilausten mukaisia tuotteen vastaanottoja ja myöhemmin toimittajan tilauksen mukaan laskuttamien laskujen kirjanpitoa.  

**Ostotilaukset**-sivulla on yleiskatsaus käytettävissä olevista tilauksista. Voit myös muokata sivulla kyseisiä tilauksia. Kun avaat ostotilauksen, voit valita **Otsikko**-näkymän, jossa on vain kerran kuhunkin ostotilaukseen määritettäviä tietoja, kuten toimittajan tiedot. Vaihtoehtoisesti voit valita **Rivit** -näkymän, jossa voi muokata tilausrivejä. Yleensä voit siirtyä näkymästä toiseen kun muokkaat POs. Kuluja ei näy suoraan **ostotilausten** sivulla mutta, käytetään valikoiden otsikkoon ja riveille.  

Ostotilauksia, tuotteen vastaanottoja ja toimittajan laskuja koskevia tietoja voi tarkastella useissa raporteissa. Nämä raportit sijaitsevat **Hankinta**- ja **Ostoreskontra**-moduuleissa.  

Voit tarkastella luetteloita ostotilausten eri vaiheissa **Ostotilauksen valmistelu**- ja **Ostotilauksen vastaanotto ja seuranta** -työtiloissa. Niissä on myös yhteenveto tehtävistä toimista. **Ostotilauksen valmistelu** -työtila keskittyy ostotilauksen luontiin ja tarkasteluun, tilauksen käsittelyyn hyväksynnän läpi ja toimittajan vahvistukseen. **Vastaanotto ja seuranta** työtilan tarkoituksena on tavaroiden tai palveluiden vastaan POs vastaanoton käsittely. Se sisältää luetteloita, jotka antavat tietoja vastaanotoista, jotka ovat myöhässä tai, josta pian tulee asianmukaisesti toimittaja vastaa toimituksesta. Näissä työtiloissa ei tehdä liittyviä vastaanottotoimintoja, jotka tehdään varastossa. Kyseiset tehtävät tehdään käyttämällä **Inventoinnin- ja varastonhallinta**- ja **Varastonhallinta**-moduulien sivuilla. Toimittajan laskut käsitellään **Toimittajan laskun syöttö** -työtilassa ja maksut tehdään **Toimittajan maksut** -työtilassa.  

Seuraavissa artikkeleissa on yhteenveto ostotilauksen vaiheista:

-   [Ostotilauksen luonti](purchase-order-creation.md)
-   [Ostotilauksen hyväksyntä ja vahvistus](purchase-order-approval-confirmation.md)
-   [Tuotteen vastaanotto ostotilausten perusteella](product-receipt-against-purchase-orders.md)
-   [Toimittajan laskujen yleiskatsaus](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)

## <a name="types-of-purchase-orders"></a>Ostotilaustyypit
On kolmenlaisia POs. Tyyppi on määritettävä luotaessa PO. Voit määrittää uusien tilausten oletustilaustyypin **Hankintaparametrit**-sivulla.

| Ostotilaustyyppi        | Kuvaus                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kirjauskansio        | Käytä tätä tyyppi oletustilauksen luontiin. Tämä tyyppi ei vaikuta varastomääriin eikä luo varastotapahtumia. Ostotilauskirjauskansion rivit eivät sisälly pääajoitukseen.                                                                                                       |
| Ostotilaus | Käytä tätä tyyppi ostotilauksen luontiin, kun tilaukset vahvistetaan toimittajalle ja kun tilauksia käsitellään vastaanotossa ja laskutuksessa ennen toimittajalle maksamista. Tämä on yleisin ostotilaustyyppi.                                                                          |
| Palautettu tilaus | Käytä tyyppiä, kun palautat tavaroita toimittajalle. Tämä tilaustyyppi edellyttää, että määrität toimittajan antaman palautusnumeron. Palautusnumero määritetään ostotilauksen **Yleiset**-välilehdessä. Tilausrivien määrien on oltava negatiivisia. |

## <a name="purchase-order-statuses"></a>Ostotilauksen tilat
Ostotilauksessa on useita tilauksen etenemistä ilmaisevia tilakenttiä. Nämä kentät näkyvät tilauksen **Otsikko**-kentässä ja muutamat näkyvät myös kaikkien tilausten ruudukkoyhteenvedossa. **Tila**-kenttä näyttää tilausmäärien tilan. Käytettävissä ovat seuraavat arvot:

-   **Avoin tilaus** – tilaukset on luotu ja määrät on tilattu.
-   **Vastaanotettu** – osa määristä on vastaanotettu, mutta niitä ei ole vielä laskutettu.
-   **Laskutettu** – tilauksen koko määrä on laskutettu. **Huomautus:** Jos tilaus on laskutettu *osittain*, **Vastaanotettu**- eikä **Laskutettu**-tila ei ole sopiva vaihtoehto. Niinpä tilauksen tila on edelleen **Avoin tilaus**.
-   **Peruutettu** – Tilaus vahvistettiin mutta peruutettiin myöhemmin. Tämän vuoksi tämä tila ilmaisee, että tilauksessa ei ole enää avoimia määriä.

Voit arvioida **Asiakirjan tila** -kentän avulla nopeasti tilauksen edistymisen käsiteltävien asiakirjojen perusteella. Se ilmaiseen tilauksen viimeisimmän valmiin asiakirjan tilan. Käytettävissä ovat seuraavat arvot:

-   **Ei mitään** – tilauksessa ei ole käsitelty vielä yhtään asiakirjaa.
-   **Ostokysely** – ostokysely on luotu ja tilaus odottaa toimittajan palautetta.
-   **Ostotilaus** – tilauksen vahvistus on käsitelty.
-   **Tuotteen vastaanotto** – tuotteen vastaanotto on käsitelty tilauksessa.
-   **Lasku** – tilauksen lasku on kirjattu.

**Hyväksynnän tila** -kenttää käytetään, kun ostotilauksen arviointiprosessin tai työnkulun aikana. Käytettävissä ovat seuraavat arvot:

-   **Luonnos**, **Tarkistuksessa** ja **Hylätty** – näitä tiloja käytetään vain, kun hyväksyntätyönkulku on käytössä ostotilauksessa.
-   **Hyväksytty** – Tämä tila määritetään tilauksille, joiden hyväksyntätyönkulku on valmis. Jos tilauksessa ei käytetä hyväksyntätyönkulkua, tilauksen tilaksi tulee heti **Hyväksytty**.
-   **Ulkoisessa tarkastelussa** – Tätä tilaa käytetään skenaarioissa, joissa ostokysely lähetetään toimittajalle, jotta toimittaja voi vahvistaa ostotilauksen ehdot. Tätä tilaa käytetään myös prosesseissa, jotka **Vahvistuspyyntö**-toiminto on käynnistänyt. Tässä prosessissa toimittajaa pyydetään vahvistamaan ostotilauksen ehdot muodostamalla yhteyden järjestelmään ja rekisteröimällä, hyväksyykö vai hylkääkö se tilauksen.
-   **Vahvistettu** – Tämä tila määritetään sen jälkeen, kun tilaus on vahvistettu. Yleensä tämä on viimeinen tilaukselle määritetty hyväksymistila.


<a name="see-also"></a>Lisätietoja
--------

[Purchase order creation](purchase-order-creation.md)

[Ostotilauksen hyväksyntä ja vahvistus](purchase-order-approval-confirmation.md)

[Tuotteen vastaanotto ostotilausten perusteella](product-receipt-against-purchase-orders.md)

[Toimittajan laskujen yleiskatsaus](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)


