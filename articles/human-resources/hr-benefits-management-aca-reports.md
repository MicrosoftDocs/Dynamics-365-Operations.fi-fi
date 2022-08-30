---
title: Luo Affordable Care Act -raportit etujen hallinnassa
description: Tässä artikkelissa käsitellään tapaa, jolla etujen hallinta seuraa Affordable Care Actin (ACA) työnantajan toimeksiannosta lomakkeella 1095-B ja lomakkeella 1095-C raportoituja tietoja.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a56fe2b3a25a300687d81702c52614a78f2a6f61
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336891"
---
# <a name="generate-aca-reports-in-benefits-management"></a>ACA-raporttien luominen etujen hallinnassa

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Etujen hallinnan avulla voidaan seurata tietoja, jotka on raportoitu Affordable Care Actin (ACA) työnantajan toimeksiannosta lomakkeella 1095-B ja lomakkeella 1095-C. Kuten ACA-raportointitoiminto vanhassa **Edut**-työtilassa, tämä toiminto koskee vain Yhdysvalloissa olevia yrityksiä.

Jotta voit käyttää näitä toimintoja, sinun on ensin otettava käyttöön **Lisäetujen hallinta**. Lisätietoja, kuten tärkeät etujen hallintaa koskevat tiedot ovat kohdassa [Etujen hallinnan ottaminen käyttöön ja poistaminen käytöstä](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> Voit käyttää ACA-raportointia vain joko **Etujen hallinta** -työtilasta tai vanhasta **Edut**-työtilasta, mutta et molemmista. Esimerkiksi jos siirryt etujenhallintaan, ACA-raportointi on käytettävissä vain **Etujen hallinta** -työtilassa, ei vanhassa **Edut**-työtilasta.
>
> Jos siirryt etujenhallintaan rekisteröitymisvuoden keskellä, sinun on määritettävä työntekijöiden tiedot oikein koko vuoden ajaksi Etujen hallinnassa. Näin varmistat, että saat koko vuoden tarkat raportointitiedot.

## <a name="getting-started"></a>Aloittaminen

Voit seurata 1095-lomakkeiden tietoja luomalla ensin yhden tai useita Affordable Care -kattavuusryhmiä. Ryhmät ilmaisevat seuraavat tiedot:

- Työntekijälle tehty kattavuustarjous.
- Työntekijän osuus pienimmän kustannuksen kuukausittaisen lisän kustannuksista, jos kustannukset ovat liittovaltion köyhyysrajan yläpuolella.
- Työnantajan käyttämä Safe Harbor (jos sovellettavissa)

Affordable Care -kattavuusryhmien avulla voit hallita näitä tietoja useille työntekijätietueille, joissa on samat ehdot. Voit helposti liittää ryhmiä yhteen tai useampiin työntekijöihin.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Affordable Care -kattavuusryhmän luominen tai muokkaaminen

1. Valitse **Etujen hallinta** -työtilasta **Affordable Care -kattavuusryhmä**.

    ![Affordable Care -kattavuusryhmän valinta.](./media/hr-benefits-management-aca-coverage-group.png)

2. Valitse **Uusi**, jos haluat luoda uuden Affordable Care -kattavuusryhmän tai muuta aiemmin luotua ryhmää valitsemalla **Muokkaa**.

    ![Valitse Uusi tai Muokkaa.](./media/hr-benefits-management-aca-new.png)

3. Määritä seuraavat kentät.

    | Kenttä | kuvaus |
    |---|---|
    | Nimi | Anna ryhmälle nimi. |
    | kuvaus | Anna ryhmän kuvaus. |
    | Kattavuustarjous | Työntekijöille, heidän aviopuolisolleen tai kumppanilleen ja heidän huollettavilleen tarjottava kattavuus. |
    | Työntekijän osa kustannuksista | Summa työntekijä, josta työntekijä vastaa. |
    | Sovellettava kohta 4980H safe harbor | Turvakoodi 4980H Safe Harbor- tai siirtohelpotuskoodi. |
    | Suunnitelman aloituskuukausi | Valitse kalenterikuukausi, jolloin etusuunnitelman vuosi alkaa. |
    | Ryhmän ensimmäinen voimassaolopvm | Tietueen ensimmäinen voimassaolopäivä. |
    | Ryhmän viimeinen voimassaolopvm | Tietueen viimeinen voimassaolopäivä. Jos erääntymispäivää ei ole, valitse **Ei koskaan**. |

    ![Kattavuusryhmän luominen.](./media/hr-benefits-management-aca-new-group.png)

4. Valitse **Tallenna**.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Usean työntekijän liittäminen Affordable Care -kattavuusryhmään

1. Valitse **Etujen hallinta** -työtilasta **Affordable Care -kattavuusryhmä**.
2. Valitse ryhmä, johon työntekijät määritetään.
3. Valitse **Joukkomääritys**.

    ![Valitse Joukkomääritys.](./media/hr-benefits-management-aca-mass-assignment.png)

4. Valitse työntekijät luettelosta ja valitse sitten **Määritä**.

    ![Valittujen työntekijöiden määrittäminen ryhmään.](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Kattavuusvaihtoehtojen useiden versioiden ylläpitäminen

Voit ylläpitää useita versioita mistä tahansa kattavuusryhmästä. Kun organisaatiossasi jokin muuttuu tai tarjotut edut muuttuvat, voit pitää ryhmän tiedot ajan tasalla ilman, että sinun ei tarvitse luoda uutta ryhmää ja määrittää siihen työntekijöitä uudelleen.

Kun olet luonut Affordable Care -kattavuusryhmät, voit määrittää niihin työntekijöitä joukkotoimintona. Voit myös liittää työntekijät ryhmiin yksitellen ja määrittää, seurataanko ja raportoidaanko ACA-tietoja.

Jos työntekijän ACA-tietoja ei tarvitse seurata ja raportoida, voit määrittää **Raportin kattavuus** -asetuksen arvoksi **Ei**. Esimerkiksi osa-aikatyöntekijöille ei aina tarvitse olla ACA-raportointia.

### <a name="override-default-values-for-an-employee"></a>Työntekijän oletusarvojen korvaaminen

Jos työntekijä on liitetty Affordable Care -kattavuusryhmään, voit muuttaa seuraavia asetuksia kuukausien osalta, jotka edellyttävät eri arvoja:

- Kattavuustarjous
- Työntekijän osa kustannuksista
- Sovellettava kohta 4980H safe harbor

> [!NOTE]
> Vuoden 2020 ACA-raporteissa on raportoitava sekä työpaikan että kotiosoitteen postinumerot lomakkeessa 1095-C. Arvot täytetään automaattisesti nykyisten aktiivisten sijaintien perusteella. Jos jompikumpi sijainti oli eri vuoden minkä tahansa osan aikana, arvo on ohitettava. 1095-C-raportin **Postinumero**-kenttä (rivi 17) täytetään vain, jos **Kattavuustarjous**-koodi sisältää **1L**–**1Q** seuraavasti:
>
> - **1L, 1M tai 1N:** Ensisijaisen asuinpaikan postinumero
> - **1O, 1P, 1Q:** Ensisijainen työn postinumero

Jos haluat määrittää poikkeuksia Affordable Care -kattavuusryhmän arvoille, noudata seuraavia ohjeita.

1. Valitse **henkilöstöhallinnan** työtilassa **linkit** ja valitse sitten **työntekijät**.
2. Valitse luettelosta työntekijä.
3. Valitse **Työsuhde**-välilehden **Lisätiedot**-osasta **Affordable Care -kattavuus**.

    ![Yhden työntekijän asetusten muuttaminen.](./media/hr-benefits-management-aca-change-single-employee.png)

4. Valitse **Muokkaa**.
5. Valitse jokaiselle muutosta edellyttävälle kuukaudelle **Ohita oletus** -valintaruutu ja muuta sitten muita arvoja tarpeen mukaan.

    ![Oletusarvojen ohitus.](./media/hr-benefits-management-aca-override-default.png)

6. Valitse **Tallenna**.

## <a name="report-health-care-coverage"></a>Terveydenhuollon kattavuuden raportointi

Sinun on seurattava kaikkia työnantajan kustantamia, itsevakuutettuja terveydenhuollon kattavuuksia kokoaikaisille ja osa-aikaisille työntekijöille. Sisällytä kukin työntekijä ja heidän huollettavansa 1095-C-raporttiin niiden kuukausien osalta, jolloin työntekijät on katettu.

Seuraavia ohjeita noudattamalla voit määrittää, onko etusuunnitelma raportoitava.

1. Valitse **Etujen hallinta** -työtilassa **Etuussuunnitelmat**.
2. Valitse raportoitava etusuunnitelma.
3. Valitse **Muokkaa**.
4. Määritä **Raportoidaan Affordable Care Act -lain mukaan** -arvoksi **Kyllä**.

    ![Terveydenhuollon kattavuuden raportointi.](./media/hr-benefits-management-aca-report-coverage.png)

5. Valitse **Tallenna**.

Jos työntekijä valitsee huollettavalleen terveyskattavuuden, huollettavan kattavuuskauden määrittää päivämäärä, jolloin huollettava on rekisteröity tai poistettu. Huollettavien kattavuuspäivämäärät lasketaan automaattisesti sen kauden perusteella, jolloin huollettava oli oikeutettu ja aktiivinen suunnitelmassa rekisteröintivuoden aikana.

## <a name="generate-1095-b-and-1095-c-forms"></a>Luo 1095-B- ja 1095-C-lomakkeita

Voit luoda ACA:n 1095-B- ja 1095-C-lomakkeita ja jakaa ne työntekijöille. Voit myös luoda sähköisesti lomakkeen 1095-C ja vastaavat 1094-C-siirtotiedostot lähetettäväksi Internal Revenue Service (IRS) -palveluun.

1. Valitse **Etujen hallinta** -työtilassa **ACA 1095-B -lomake** tai **ACA 1095-C -lomake**.
2. Muuta parametreja tarpeen mukaan ja valitse sitten **OK**.

    > [!NOTE]
    > Jos tulostat 1095-C-lomakkeet yli 500 työntekijälle, PDF-tiedostoja on useita. **Tiedostonhallinnan parametrit** -sivun **Tiedoston enimmäiskoko megatavuina** -kentän arvo on suositeltavaa suurentaa arvoksi **150**. (Sivu voidaan avata nopeasti siirtymispalkin hakukentän avulla.)
    >
    > ![Tiedoston enimmäiskoon muuttaminen.](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Voit tarkistaa raporttien tilan ja tarkastella niitä avaamalla **Sähköisen raportoinnin työt** -sivun siirtymispalkin hakukentän avulla.

    ![Sähköisen raportoinnin työt -sivun hakeminen.](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Valitse näytettävä raportti ja valitse sitten **Näytä tiedostot**.

    ![Tiedostojen näyttäminen.](./media/hr-benefits-management-aca-show-files.png)

5. Valitse **Avaa**.

    ![Tiedoston avaaminen.](./media/hr-benefits-management-aca-open-file.png)

6. Avaa zip-tiedosto ja valitse raportti selaimen ikkunan alaosassa näkyvästä ilmoitusrivistä. Voit tarkastella tai tulostaa PDF-tiedoston.

    ![Esimerkki 1095-C-lomakkeesta.](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>ACA-kattavuustietojen tarkasteleminen

**Työntekijöiden Affordable Care -kattavuus** -sivulla näkyvät seuraavat tiedot:

- Kuhunkin kattavuusryhmään liitetyt työntekijät
- Työntekijät, joiden ei tarvitse sisältyä raporttiin
- Määrittämättömät työntekijät

Näitä tietoja voi tarkastella seuraavasti.

1. Valitse **Etujen hallinta** -työtilasta **Työntekijöiden Affordable Care -kattavuus**.
2. Valitse **Ryhmän nimi**-kentässä ryhmä.

    ![ACA-kattavuuden tarkasteleminen.](./media/hr-benefits-management-aca-view-coverage.png)

Jos jokin Affordable Care -kattavuusryhmän oletusarvoista on korvattu, muutetun arvon vieressä näkyy tähtimerkki. Jos jokaisen 12 kuukauden arvo on sama eikä sitä ole korvattu, arvo näkyy **Kaikki 12 kuukautta** -sarakkeessa.

Voit tarkastella työntekijöitä, jotka on merkitty ACA-raportoinnin ulkopuolle ja jotka eivät vaadi lomaketta 1095-C. Valitse **Suodatusperuste**-kentässä **Ei ACA-raportoitava**.

Voit tarkastella työntekijöitä, joita ei ole liitetty ryhmään tai jotka on liitetty vanhentuneeseen ryhmään. Valitse **Suodatusperuste**-kentässä mukaan **Ei määritetty tai vanhentunut ryhmä**.

### <a name="export-to-excel"></a>Vie Exceliin

Voit viedä minkä tahansa luettelon Microsoft Exceliin seuraavien ohjeiden mukaan.

1. Valitse **Avaa Microsoft Officessa** -painike.
2. Valitse **HCM Human Resources – väliaikainen taulu sisäiseen käyttööön**.
3. Valitse **Lataa**.

### <a name="view-aca-reportable-dependents"></a>ACA-raportoitavien huollettavien tarkasteleminen

Jos sinun on raportoitava kattavuuteen kuuluvat henkilöt itsevakuutettujen kattavuuden vuoksi, voit tarkastella huollettavia, jotka on katettu **ACA-raportoitaviksi** merkityissä etusuunnitelmissa. Valitse toimintoruudussa **Näytä huollettavien kattavuus**.

![Huollettavien kattavuuden tarkasteleminen.](./media/hr-benefits-management-aca-view-dependent-coverage.png)

Näkyviin tulee työntekijän huollettavien kattavuustiedot.

![Huollettavan kattavuus.](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Sivulla näkyvät vain ne edut, jotka on merkitty **ACA-raportoitaviksi**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
