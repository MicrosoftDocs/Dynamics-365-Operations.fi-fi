---
title: Määritä TDS-viranomaisen maksujen toimitusmaksut
description: Tässä artikkelissa on tietoja siitä, miten määritetään Vero vähennettynä lähteissä (TDS) -viranomaisen maksujen toimitusmaksut.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 598d4c07d9f96fb5ae58c3929bab353a6d57615f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845216"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>Määritä TDS-viranomaisen maksujen toimitusmaksut

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja siitä, miten määritetään Vero vähennettynä lähteissä (TDS) -viranomaisen maksujen toimitusmaksut.

1. Siirry kohtaan **Ostoreskontra \> Maksun asetukset \> Toimitusmaksu**.

    [![Toimitusmaksu-sivu.](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Luo toimitusmaksu valitsemalla **Uusi** ja kirjoita tarvittavat tiedot.
3. Valitse toimitusmaksun tyyppi **Maksun tyyppi** -kentästä:

    - **None**
    - **Korko** – Korko veloitetaan TDS-viranomaistoimittajalle suoritetuista myöhästyneistä maksuista.
    - **Muut** – Muut maksut veloitetaan TDS-viranomaistoimittajalle suoritetuista myöhästyneistä maksuista.

    Jos valitset **Korko** tai **Muut**, **Maksu**-kentän arvoksi tulee automaattisesti **Kirjanpito**.

4. Jos valitset **Korko** tai **Muut** **Kenttätyyppi**-kentässä **Päätili**-kentässä valitse kirjanpitotili, jolle korko tai muut kulut kirjataan.
5. Lisää muut pakolliset tiedot.
6. Avaa **Toimitusmaksujen asetukset** -sivu valitsemalla **Toimitusmaksujen asetukset** toimintoruudussa. Sivulla voit määrittää toimitusmaksut erilaisille pankkien, maksutapojen, maksuerittelyjen, valuuttojen ja päivämäärävälien yhdistelmille.

    [![Toimitusmaksujen asetukset -sivu.](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. Määritä **Yhteenveto**-välilehden **Ryhmittelyt**-kentässä pankit, joille olet määrittänyt toimitusmaksun:

    - **Taulukko** – Maksu on voimassa tietylle pankkitilille.
    - **Ryhmä** – Maksu on voimassa tietylle pankkiryhmälle.
    - **Kaikki** – maksu on voimassa kaikille pankkitileille.

8. Jos valitsit **Ryhmittelyt**-kentästä **Taulukko** tai **Ryhmä**, valitse **Pankkisuhde**-kentästä tietty pankkitili tai pankkiryhmä, jolle olet määrität toimitusmaksun.
9. Valitse **Maksutapa**-kentässä maksutapa, jota maksujen maksamiseen käytetään.
10. Valitse tai lisää **Maksumäärittely**-kentässä **Maksumäärittely**-sivulla luotu maksumäärittelykoodi.
    - Maksumäärittelyä käytetään sähköisen rahansiirron maksutavoissa.
12. Valitse **Maksun valuutta** -kentässä maksun aktivoiva valuutta. Vain valittua valuuttaa käyttävät tapahtumat voivat aktivoida maksun. Jos jätät tämän kentän tyhjäksi, kaikki valuutat aktivoivat maksun.
13. Valitse laskentatapa **Prosentti/Summa**-kentästä. Vaihtoehdot ovat **Summa**, **Prosentti** ja **Väli**.
14. Määritä **Maksun summa** -kenttään maksun summa joko maksun prosenttiosuutena tai yhden maksun summana.
15. Valitse **Maksun valuutta** -kentässä maksun valuuttakoodi.
16. Valitse **Yleinen**-välilehti, jos haluat tarkastella tai muokata valitun pankkitilin tietoja.

    [![Yleinen-välilehti.](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. Kirjoita **Vähintään**-kenttään tapahtuman vähimmäissumma, joka aktivoi maksun.
17. Kirjoita **Enintään**-kenttään tapahtuman enimmäissumma, joka aktivoi maksun.
18. Määritä **Päivämäärästä**- ja **Päivämäärään**-kenttiin maksujen laskennan päivämääräväli.
19. Määritä **Vähimmäissumma**-kenttään maksun summa joko maksun prosenttiosuutena tai yhden maksun summana.
20. Valitse **Arvonlisäveroryhmä**-kentässä arvonlisäveroryhmä, jonka avulla maksun summan arvonlisävero lasketaan.
21. Valitse **Nimikkeen arvonlisäveroryhmä**-kentässä nimikkeen arvonlisäveroryhmä, jonka avulla maksun summan nimikkeen arvonlisävero lasketaan.
22. Valitse **Väli**-välilehti. 

    [![Väli-välilehti.](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. Kirjoita maksun kirjauspäivämäärän (alennuksen päivämäärän) ja velkakirjan eräpäivän välinen aika päivinä **Päivää**-kenttään.
24. Valitse **Prosentti/summa**-kentässä, onko määritys prosentti vai määritetty summa.
25. Määritä **Maksun summa**-kenttään maksun summa joko maksun prosenttiosuutena tai yhden maksun summana.
26. Sulje **Toimitusmaksujen asetukset** -sivu.
27. Sulje **Toimitusmaksu**-sivu.
