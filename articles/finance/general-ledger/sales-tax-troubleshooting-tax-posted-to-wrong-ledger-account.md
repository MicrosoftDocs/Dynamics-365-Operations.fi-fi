---
title: Vero kirjataan tositteen väärälle kirjanpitotilille
description: Tässä aiheessa on vianmääritystietoja, jotka voivat auttaa, kun vero kirjataan tositteen väärälle kirjanpitotilille.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020088"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Vero kirjataan tositteen väärälle kirjanpitotilille

[!include [banner](../includes/banner.md)]

Kirjaamisen aikana vero saatetaan kirjata tositteen väärälle kirjanpitotilille. Voit ratkaista tämän ongelman noudattamalla seuraavien osien ohjeita tarpeen mukaan. Tämän ohjeaiheen esimerkeissä myyntitilausta käytetään liiketoiminta-asiakirjana.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Etsi virheellisen verotapahtuman verokoodi

1. Valitse **Tositetapahtumat**-sivulla tapahtuma, jota haluat käyttää, ja valitse sitten **Kirjattu arvonlisävero**.

    [![Kirjattu arvonlisävero -painike Tositetapahtumat-sivulla](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. Tarkista arvo **Arvonlisäverokoodi**-kentässä. Tässä esimerkissä se on **VAT 19**.

    [![Kirjattu arvonlisävero -sivun Arvonlisävero-kenttä](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Tarkista verokoodin kirjanpidon kirjausryhmä

1. Valitse **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäverokoodit**.
2. Etsi ja valitse verokoodi sekä tarkista sitten **Kirjanpidon kirjausryhmä** -kentän arvo. Tässä esimerkissä se on **VAT**.

    [![Kirjanpidon kirjausryhmä -kenttä Arvonlisäverokoodit-sivulla](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. **Kirjanpidon kirjausryhmä** -kentän arvo on linkki. Jos haluat tarkastella ryhmän konfiguraation tietoja, valitse linkki. Vaihtoehtoisesti voit valita ja pitää kenttää painettuna (tai napsauttaa sitä hiiren kakkospainikkeella) ja valita sitten **Näytä tiedot**.

    [![Näytä tietoja -komento](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. Varmista **Maksettava arvonlisävero** -kentässä, että tilinumero on oikea tapahtumalajin mukaan. Valitse sitten oikea tili, jolle kirjaat sen. Tässä esimerkissä myyntitilauksen arvonlisävero on kirjattava arvonlisäveron kulutilille 222200.

    [![Maksettava arvonlisävero -kenttä Kirjanpidon kirjausryhmät -sivulla](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    Seuraavassa taulukossa on tietoja kustakin **Kirjanpidon kirjausryhmät** -sivun kentästä.

    | Kenttä                  | kuvaus |
    |------------------------|-------------|
    | Maksettava arvonlisävero      | Veroviranomaiselle maksettavan lähtevän arvonlisäveron päätili. |
    | Saatava arvonlisävero   | Veroviranomaiselta saatavien saapuvien verojen päätili. |
    | Käyttöverokulu        | Päätili, jota käytetään vähennyskelpoisten käyttöverojen kirjaamiseen, joita toimittajat eivät peri tai raportoi veroviranomaiselle osana Euroopan unionin (EU) käänteistä arvonlisäveroa (GST) / harmonisoitua arvonlisäveroa (HST). Tapahtumassa käytettävän arvonlisäveroryhmän arvonlisäverokoodin **Käyttövero**-vaihtoehto on valittava. Tämä kenttä ei ole käytettävissä, jos **Käytä arvonlisäverotuksen sääntöjä** -vaihtoehto on valittu **Kirjanpitoparametrit**-sivulla. |
    | Käyttöverovelka        | Päätili, jota käytetään veroviranomaisille maksettavien saapuvien käyttöverojen kirjaaminen. |
    | Maksutili     | Päätili, jolle **Maksettava käyttövero**- ja **Saatava arvonlisävero** -kentässä määritettyjen kirjanpitotilien nettosaldo kirjataan. |
    | Toimittajan käteisalennus   | Päätili, jonne tähän kirjanpidon kirjausryhmän liitetyn arvonlisäverokoodin käteisalennukset kirjataan. |
    | Asiakastapauksen alennus | Päätili, jonne tähän kirjanpidon kirjausryhmän liitetyn arvonlisäverokoodin käteisalennukset kirjataan. |

    Lisätietoja on kohdassa [Arvonlisäveron kirjanpidon kirjausryhmien määrittäminen](tasks/set-up-ledger-posting-groups-sales-tax.md).

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Kirjanpitodimensioiden tarkistus koodin virheenkorjauksella

Koodissa kirjaustili määräytyy kirjanpitodimension mukaan. Kirjanpitodimensio tallentaa tilin tietuetunnuksen tietokantaan.

1. Lisää myyntitilauksen keskeytyskohta **Tax::saveAndPost()**- ja **Tax::post()** -menetelmiin. Kiinnitä huomiota **\_ledgerDimension**-arvoon.

    [![Myyntitilauksen koodinäyte, jossa on keskeytyskohta](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    Lisää ostotilauksessa keskeytyskohta **TaxPost::saveAndPost()**- ja **TaxPost::postToTaxTrans()**-menetelmiin. Kiinnitä huomiota **\_ledgerDimension**-arvoon.

    [![Ostotilauksen koodinäyte, jossa on keskeytyskohta](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Suorita seuraava SQL-kysely, kun haluat etsiä tietokannan tilin näyttöarvon, joka perustuu kirjanpitodimension tallentamaan tietuetunnukseen.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Tietuetunnuksen näyttöarvo](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. Voit tarkistaa kutsupinon ja selvittää, mihin **_ledgerDimension** on määritetty. Yleensä arvo on peräisin kohteesta **TmpTaxWorkTrans**. Tässä tapauksessa sinun on lisättävä keskeytyskohta kohteisiin **TmpTaxWorkTrans::insert()** ja **TmpTaxWorkTrans::update()** etsiäksesi, minne arvo on määritetty.

## <a name="determine-whether-customization-exists"></a>Määritä, onko mukautus olemassa

Jos olet suorittanut edellisten osien vaiheet, mutta et ole löytänyt ongelmaa, selvitä, onko mukautus olemassa. Jos mukautusta ei ole, luo Microsoftin huoltopyyntö lisätuen saamiseksi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
