---
title: Ostotilausten yleiskatsaus
description: Tässä artikkelissa on yleisiä tietoja ostotilauksista ja linkkejä muita ostotilauksen eri vaiheita käsitteleviin artikkeleihin.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder, PurchConfirmationRequestJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "93083"
- intro-internal
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d589737fd57d0ceeb7c147f8d5fe322682acf50
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675960"
---
# <a name="purchase-order-overview"></a>Ostotilausten yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleisiä tietoja ostotilauksista ja linkkejä muita ostotilauksen eri vaiheita käsitteleviin artikkeleihin.

Ostotilaus on asiakirja, joka ilmaisee toimittajan kanssa tehdyn sopimuksen hyödykkeiden tai palvelujen ostamisesta. Asiakirjan avulla voi myös seurata tilausten mukaisia tuotteen vastaanottoja ja myöhemmin toimittajan tilauksen mukaan laskuttamien laskujen kirjanpitoa.  

**Ostotilaukset**-sivulla on yleiskatsaus käytettävissä olevista tilauksista. Voit myös muokata sivulla kyseisiä tilauksia. Kun avaat ostotilauksen, voit valita **Otsikko**-näkymän, jossa on vain kerran kuhunkin ostotilaukseen määritettäviä tietoja, kuten toimittajan tiedot. Vaihtoehtoisesti voit valita **Rivit** -näkymän, jossa voi muokata tilausrivejä. Yleensä ostotilausta muokatessa vaihdellaan näiden näkymien välillä. Muutosluetteloa ei ole suoraan **Ostotilaukset**-sivulla, vaan niitä käytetään tilausotsikon ja -rivien valikoista.  

Ostotilauksia, tuotteen vastaanottoja ja toimittajan laskuja koskevia tietoja voi tarkastella useissa raporteissa. Nämä raportit sijaitsevat **Hankinta**- ja **Ostoreskontra**-moduuleissa.  

Voit tarkastella luetteloita ostotilausten eri vaiheissa **Ostotilauksen valmistelu**- ja **Ostotilauksen vastaanotto ja seuranta** -työtiloissa. Niissä on myös yhteenveto tehtävistä toimista. **Ostotilauksen valmistelu** -työtila keskittyy ostotilauksen luontiin ja tarkasteluun, tilauksen käsittelyyn hyväksynnän läpi ja toimittajan vahvistukseen. **Ostotilauksen vastaanotto ja seuranta** -työtila keskittyy ostotilausten mukaisten hyödykkeiden tai palvelujen vastaanottoon. Siinä on luetteloita, joissa on tietoja myöhästyneistä vastaanotoista tai vastaanotoista, jotka toimittaja on pian toimittamassa. Näissä työtiloissa ei tehdä liittyviä vastaanottotoimintoja, jotka tehdään varastossa. Kyseiset tehtävät tehdään käyttämällä **Inventoinnin- ja varastonhallinta**- ja **Varastonhallinta**-moduulien sivuilla. Toimittajan laskut käsitellään **Toimittajan laskun syöttö** -työtilassa ja maksut tehdään **Toimittajan maksut** -työtilassa.  

Seuraavissa artikkeleissa on yhteenveto ostotilauksen vaiheista:

-   [Ostotilausten luominen](purchase-order-creation.md)
-   [Ostotilausten hyväksyminen ja vahvistaminen](purchase-order-approval-confirmation.md)
-   [Tuotteen vastaanotto ostotilausten perusteella](product-receipt-against-purchase-orders.md)
-   [Toimittajan laskujen yleiskatsaus](../../finance/accounts-payable/vendor-invoices-overview.md)

## <a name="types-of-purchase-orders"></a>Ostotilaustyypit
Ostotilaustyyppejä on kolme. Tyyppi on määritettävä ostotilauksen luomisen yhteydessä. Voit määrittää uusien tilausten oletustilaustyypin **Hankintaparametrit**-sivulla.

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


## <a name="additional-resources"></a>Lisäresurssit

[Ostotilausten luominen](purchase-order-creation.md)

[Ostotilausten hyväksyminen ja vahvistaminen](purchase-order-approval-confirmation.md)

[Tuotteen vastaanotto ostotilausten perusteella](product-receipt-against-purchase-orders.md)

[Toimittajan laskujen yleiskatsaus](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]