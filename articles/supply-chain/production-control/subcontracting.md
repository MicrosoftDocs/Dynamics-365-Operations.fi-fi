---
title: Alihankinta
description: Tämä ohjeaihe opastaa tuotannon alihankinnan ohjeen luomisesta Microsoft Dynamics 365 for Finance and Operationsissa.
author: christophernread
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55b516f928eadea9b7ddbb1192db79f3ab7fa204
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "336701"
---
# <a name="subcontracting"></a>Alihankinta

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe opastaa tuotannon alihankinnan ohjeen luomisesta Microsoft Dynamics 365 for Finance and Operationsissa. Tämän ohjeaiheen ensimmäisessä osassa kuvataan tietojen määrittämistä. Toisessa osassa selvitetään esittelyn vaiheita.

## <a name="target-audience"></a>Kohdeyleisö

Tässä ohjeaiheessa kerrotaan, miten voit määrittää valmistuksen alihankinnan. Voit tehdä alihankintatoiminnon työnkulun perusmäärityksen HQUS-yrityksen olemassa olevien tietojen avulla. HQUS-yrityksen esittelytiedot sisältävät asetusparametreja, jotka on määritetty etukäteen esittelyn vaiheiden tukemiseksi. Vaikka esittelyssä käsitellään erilaisten roolien tärkeimpiä heikkouksia ja haasteita, järjestelmänvalvoja voi täydentää esittelyä.

## <a name="demo-scenario"></a>Esittelyskenaario

HQUS-yrityksessä valmistetaan korkealaatuisia kaiuttimia. Valmistusprosessin aikana kaiuttimet kulkevat seuraavan kolmen työvaiheen läpi.

- **Alustava kokoonpano** – Kaiuttimen kotelon kokoaminen. Kotelon materiaali valitaan materaalivarastosta ennen työvaiheen aloittamista.
- **Pinnoitus** – Kun kaiuttimen kotelo on koottu, se on pinnoitettava. Tämän työvaiheen suorittaa toimittaja (alihankkija). Alustavasti koottu kaiuttimen kotelo lähetetään pinnoituksesta vastaavalle alihankkijalle kahden materiaalin kanssa.
- **Viimeistely** – Kun alihankkija on pinnoittanut alustavasti kootun kaiuttimen kotelon, se palautetaan HQUS-yritykselle kaiuttimen lopullista kokoamista varten.

Seuraavassa kuvassa näytetään kolme työvaihetta ja materiaalit, joita niissä käytetään.

![Alustavan kokoamisen, pinnoituksen ja viimeistelyn työvaiheet sekä niissä käytetyt materiaalit](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Määritys

Ennen esittelyn aloittamista on määritettävä tiedot.

### <a name="set-up-the-finished-product"></a>Valmiin tuotteen määrittäminen

Tässä menettelyssä käydään läpi julkaistun tuotteen D8100, "Pinnoitettu kotelo", määritystä.

1. Valitse **Tuotetietojen hallinta \>Tuotteet \>Julkaistut tuotteet**, jotta voit avata **Julkaistun tuotteen tiedot** -sivun.
2. Hae olemassa olevaa julkaistua tuotetta kirjoittamalla pikasuodatinkenttään **D8100**.

    ![Julkaistun tuotteen D8100 suodattaminen Julkaistun tuotteen tiedot -sivulle](./media/subcontract02_filtering-released-products.png)

3. Valitse toimintoruudun **Suunnittele**-välilehdessä **Reititys**, jotta voit avata **Reititys**-sivun.

    **Reititys**-sivu näyttää julkaistun tuotteen D8100 kahdeksan reititysversiota. Kahdeksan reititysversiota jaetaan neljän reitityksen välille toimipaikassa 1 ja toimipaikassa 5. Reititystä 000400 käytetään kustannuslaskentaan, reititystä 00041 käytetään, kun pinnoitus on sisäinen työvaihe, ja reititystä 00042 käytetään, kun pinnoitus on ulkoinen työvaihe.

    ![Kahdeksan reititysversioita Reititys-sivulla](./media/subcontract03_route-page.png)

4. Valitse **Versiot**-ruudukon yläruudussa reititysversio **00042** toimipaikalle **5**.
5. Valitse **Yleiskatsaus**-välilehden alemmassa ruudussa työvaihe **20** (**Cbnt CtSc**) ruudukossa.

    ![Työvaihe 20 reititysversiolle 00042 toimipaikalle 5 valittu](./media/subcontract04_route-version-operation.png)

6. Valitse **Yleinen**-välilehti.

    Huomaa, että **Reititystyyppi**-kentän arvoksi on määritetty **Toimittaja**. Tämä arvo ilmaisee, että työvaihe 20 (Cbnt CtSc) suoritetaan alihankintana.

    ![Reititystyypin kentän arvoksi on määritetty Toimittaja Yleiset-välilehdessä](./media/subcontract05_general-tab.png)

7. Valitse **Resurssivaatimukset**-välilehti.

    Ominaisuuksia käytetään löytämään sovellettava resurssi tuotantosuunnittelun aikana. Huomaa työvaiheen 20 (Cbnt CtSc) osalta, että resurssi, jolla on kaksi ominaisuutta, **pinnoitus** ja **pinnoitetut kotelot**, on pakollinen.

    ![Pinnoitus- ja pinnoitetut kotelot -ominaisuudet Resurssivaatimukset-välilehdessä](./media/subcontract06_resource-requirements-tab.png)

8. Valitse **Sovellettavat resurssit**, jotta voit avata **Sovellettavat resurssit** -valintaikkunan.

    Löytyy kolme resurssia, jotka vastaavat työvaiheen resurssivaatimuksia. Huomaa, että resurssit 8851 ja 8852 ovat **Toimittaja**-tyyppiä.

    ![Kolme asianmukaista resurssia Sovellettavat resurssit -valintaikkunassa](./media/subcontract07_applicable-resources-dialog.png)

9. Valitse **OK**, jotta voit sulkea **Sovellettavat resurssit** -valintaikkunan, ja palaa **Reititys**-sivulle.
10. Sulje **Reititys**-sivu, jotta voit palata **Julkaistun tuotteen tiedot** -sivulle.

    ![Julkaistun tuotteen tiedot -sivu](./media/subcontract08_released-product-details-page.png)

11. Valitse toimintoruudun **Suunnittele**-välilehdessä **Tuoterakenneversiot**, jotta voit avata **Tuoterakenneversiot**-sivun.

    **Tuoterakenneversiot**-sivulla on julkaistun tuotteen D8100 neljä tuoterakenneversiota. Tuoterakennetta 000040 käytetään kustannuslaskentaan ja suunnitteluun, tuoterakennetta 000041 käytetään, jos pinnoituksen työvaihe suoriteaan yrityksen sisällä, ja tuoterakenteita 000042 ja 000043 käytetään, jos pinnoituksen työvaihe suoritetaan alihankintana.

    Huomaa, että nimike S8050 on **Palvelu**-nimiketyyppinen tuote. Tämä nimike edustaa alihankintana suoritettavaa työtä.

    ![Neljä tuoterakenneversiota Tuoterakenneversiot-sivulla](./media/subcontract09_bom-versions-page.png)

12. Valitse **Tuoterakennerivit**-pikavälilehdestä **Muokkaa**, jotta voit avata **Muokkaa tuoterakenneriviä** -valintaikkunan.

    Kun tuotantotilaus on luotu ja arvioitu julkaistulle tuotteelle D8100, nimikkeelle S8050 luodaan automaattisesti ostotilaus. Tämä ostotilaus linkitetään tuotantotilaukseen. Jotta ostotilaukset voidaan luoda automaattisesti, **Rivityyppi**-kentän arvoksi on määritettävä **Toimittaja**, ja alihankkijalle on valittava toimittajatili. Tässä tapauksessa toimittajatili on US-801.

    Huomaa, että tuoterakennerivi on liitetty pinnoituksen työvaiheeseen työvaihenumeron kautta (tässä tapauksessa 20).

    ![Tuoterakennerivin valintaikkunan muokkaaminen](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Salasanan luominen varastotyöntekijöille

Sinun on määritettävä salasana varastotyöntekijöille, jotka käyttävät käsikäyttöisiä laitteita.

1. Valitse **Varaston hallinta \> Määritys \> Työntekijä**, jotta voit avata **Työn käyttäjät** -sivun.
2. Valitse **Käyttäjät**-pikavälilehdestä rivi käyttäjälle **51**.

    ![Työn käyttäjät -sivu](./media/subcontract11_work-users-page.png)

3. Valitse **Nollaa salasana**.
4. Syötä **Salasana**- ja **Vahvista salasana** -kenttiin **1**.
5. Valitse **Määritä salasana**.

## <a name="step-by-step-walkthrough"></a>Vaiheittainen esittely

**Skenaario ja tausta**

Tuotteelle D8100 luodaan 10 osan tuotantotilaus, "Pinnoitettu kotelo". Kotelot pinnoitetaan alihankintana, jonka suorittaa toimittaja US-801, Perfect Coating Solutions. Tuotantotilaus sisältää kolme työvaihetta. Ensimmäisessä työvaiheessa kotelo kootaan alustavasti yrityksen sisällä. Alustavan kokoonpanon materiaali vapautetaan keräystä varten raakamateriaalin varastossa. Kun alustava kokoonpano on valmis, alustavasti koottu kotelo lähetetään Perfect Coating Solutionsille niiden kahden materiaalin kanssa, joita tarvitaan pinnoituksen työvaiheessa. Kun pinnoitettu kotelo on saatu takaisin toimittajalta, se viedään lopullisen sisäisen kokoonpanon työvaiheen läpi, ennen kuin se ilmoitetaan valmiiksi.

1. Valitse **Tuotannonhallinta \> Tuotantotilaukset \> Kaikki tuotantotilaukset**, jotta voit avata **Kaikki tuotantotilaukset** -sivun.
2. Valitse toimintoruudussa **Uusi tuotantotilaus**, jotta voit avata **Luo tuotantotilaus** -valintaikkunan.

    ![Tuotantotilaus-valintaikkunan luominen](./media/subcontract12_create-production-order-dialog.png)

3. Valitse **Nimikkeen numero** -kentässä **D8100**.
4. Kun olet valinnut nimikkeen numeron, näkyviin tulevat varastodimension kentät. Valitse **Väri**-kentässä **Kromi**.

    Näyttöön tulee viestiruutu, jossa tiedustellaan, onko tuoterakenteen aktiiviset versiot ja reititys sisällytettävä.

    ![Viestiruutu](./media/subcontract13_message-box.png)

5. Valitse **Kyllä**. 

    **Luo tuotantojärjestys** -valintaikkunassa tuoterakenteen aktiiviset versiot ja reititys tuotteelle D8100 valitaan automaattisesti **Tuoterakenteen numero**- ja **Reititysnumero**-kentissä. Tässä tapauksessa valitaan tuoterakenne **000040** ja reititys **000040**.
    
    > [!NOTE]
    > Versiota 000040 käytetään sekä tuoterakenteelle että reititykselle kustannuslaskentaan ja suunnitteluun.

6. Valitse **Toimipaikka**-kentässä **5**.
7. Valitse **Varasto**-kentässä **51**.
8. Muuta **Tuoterakenteen numero**- ja **Reititysnumero**-kentissä arvoa, joksi valittiin automaattisesti **000042**.

    > [!NOTE]
    > Versiota 000042 käytetään sekä tuoterakenteelle että reititykselle kotelon siirtämiseksi alihankintaan toimittajalle US-801.

    ![Luo tuotantotilaus -valintaikkunassa määritetyt arvot](./media/subcontract14_create-production-order-dialog-set.png)

9. Valitse **Luo** tuotantotilauksen luomiseksi ja palaa **Kaikki tuotantotilaukset** -sivulle.

    ![Uusi tuotantotilaus Kaikki tuotantotilaukset -sivulla](./media/subcontract15_new-production-order.png)

10. Valitse toimintoruudun **Tuotantotilaus**-välilehdessä **Arvio**, jotta voit avata **Arvio**-valintaikkunan.

    ![Arvio-valintaikkuna](./media/subcontract16_estimate-dialog.png)

11. Valitse **OK** arvion vahvistamiseksi ja palaa **Kaikki tuotantotilaukset** -sivulle.

    > [!NOTE]
    > Kun tuotantotilaus on arvioitu, toimittajalle US-801 luodaan palvelunimikkeen S8050 ostotilaus.

12. Valitse toimintoruudun **Tuotantotilaus**-välilehdessä **Tuoterakenne**, jotta voit avata **Tuoterakenne**-sivun. Voit täällä tarkastella tuotantotilauksen tuoterakennerivejä.

    Huomaa palvelunimikkeen S8050 osalta, että täällä on viittaus ostotilaukseen, joka luotiin tuotantotilauksen arvioinnin yhteydessä.

    ![Tuotantotilauksen tuoterakennerivit Tuoterakenne-sivulla](./media/subcontract17_production-order-bom-lines.png)

13. Sulje **Tuoterakenne**-sivu, jotta voit palata **Kaikki tuotantotilaukset** -sivulle.
14. Valitse toimintoruudun **Aikataulu**-välilehdessä **Ajoita työt**, jotta voit avata **Työn ajoitus** -valintaikkunan.
15. Määritä seuraavat arvot:

    - Valitse **Ajoituksen suunta** -kentässä **Huomisesta päivästä eteenpäin**.
    - Määritä **Rajallinen kapasiteetti** -vaihtoehdoksi **Kyllä**.

    ![Työn ajoitus -valintaikkuna](./media/subcontract18_job-scheduling-dialog.png)

16. Valitse **OK**, jotta voit sulkea **Työn ajoitus** -valintaikkunan ja palata **Kaikki tuotantotilaukset** -sivulle.
17. Valitse toimintoruudun **Aikataulu**-välilehdessä **Gantt**, jotta voit avata **Gantt-kaavio – Resurssinäkymä** -sivun.

    Gantt-kaavio tarjoaa visuaalisen yleiskatsauksen siitä, miten tuotannon töitä ajoitetaan resursseissa. Huomaa, että ulkoinen pinnoituksen työvaihe koostuu kolmesta työstä: prosessityöstä, kuljetustyöstä ja jonoaikatyöstä.

    ![Gantt-kaavio – Resurssinäkymä-sivu](./media/subcontract19_gantt-chart.png)

18. Sulje **Gantt-kaavio – Resurssinäkymä**-sivu, jotta voit palata **Kaikki tuotantotilaukset** -sivulle.
19. Valitse toimintoruudun **Tuotantotilaus**-välilehdestä **Vapauta**, jotta voit avata **Vapauta**-valintaikkunan.

    ![Vapauta-valintaikkuna](./media/subcontract20_release-dialog.png)

20. Valitse **OK**, jotta voit sulkea **Vapauta**-valintaikkunan.
21. Valitse **Tuotannonhallinta \> Kausittaiset tehtävät \> Vapauta varastoon \> Tuoterakenteen ja lomakerivien automaattinen vapauttaminen**, jotta voit avata **Tuoterakenteen ja lomakkeen rivien automaattinen vapautus** -valintaikkunan.

    ![Tuoterakenteen ja lomakkeen rivien automaattinen vapautus -valintaikkuna](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Valitse **OK**, jotta voit suorittaa tuoterakenteen ja lomakkeen rivien automaattisen vapautustyön.

    Tämä työ vapauttaa raakamateriaalien keräystyön varastoon.

23. Valitse **Tuotannonhallinta \> Tuotantotilaukset \> Kaikki tuotantotilaukset**, jotta voit avata **Kaikki tuotantotilaukset** -sivun.
24. Valitse pikasuodatinkentän avulla tuotantotilaus, jonka parissa olet työskennellyt.
25. Valitse toimintoruudun **Varasto**-välilehdessä **Työn tiedot**, jotta voit avata **Työ**-sivun.

    Huomaa, että sivulla näkyy kaksi työjoukkoa raakamateriaalin keräykseen. Ensimmäinen työ on materiaaleille M8100 ja M8101. Näitä materiaaleja käytetään työvaiheessa 10. Toinen työ on materiaaleille M8202 ja M8250. Näitä materiaaleja käytetään työvaiheessa 20, joka on alihankintana suoritettava työvaihe.

    ![Kaksi työjoukkoa raakamateriaalin keräykseen Työ-sivulla](./media/subcontract22_work-page.png)

26. Käynnistä varastosovellus varastotyön käsittelemiseksi työvaiheelle 10.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. Valitse **Tuotannonhallinta \> Tuotantotilaukset \> Kaikki tuotantotilaukset**, jotta voit avata **Kaikki tuotantotilaukset** -sivun.
28. Valitse pikasuodatinkentän avulla tuotantotilaus, jonka parissa olet työskennellyt.
29. Valitse toimintoruudun **Tuotantotilaus**-välilehdestä **Käynnistä**, jotta voit avata **Käynnistä**-valintaikkunan.
30. Määritä **Yleiset**-välilehdelle seuraavat arvot:

    - Valitse **Työvaiheesta nro** -kentässä **10**.
    - Valitse **Työvaiheeseen nro** -kentässä **10**.

    ![Yleiset-välilehdessä määritetyt arvot](./media/subcontract23_start-dialog.png)

31. Valitse **OK**, jotta voit sulkea **Käynnistä** -valintaikkunan ja palata **Kaikki tuotantotilaukset** -sivulle.

    Huomaa, että tuotantotilauksen tilana on nyt **Käynnistetty**. Työvaiheen 10 materiaalit käytetään keräysluettelokirjauskansion automaattisessa kirjauksessa. Työvaiheen 10 ajankäyttö lasketaan reitityskorttikirjauskansion automaattisen kirjauksen mukaan.

32. Käynnistä varastosovellus varastotyön käsittelemiseksi työvaiheelle 20.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. Valitse toimintoruudun **Tuotantotilaus**-välilehdestä **Käynnistä**, jotta voit avata **Käynnistä**-valintaikkunan.
34. Määritä **Yleiset**-välilehdelle seuraavat arvot:

    - Valitse **Työvaiheesta nro** -kentässä **20**.
    - Valitse **Työvaiheeseen nro** -kentässä **20**.
    - Kirjoita **Määrä**-kenttään **10**.
    - Määritä **Kirjaa keräysluettelo nyt** -vaihtoehdon arvoksi **Ei**.

    ![Yleiset-välilehdessä määritetyt arvot](./media/subcontract24_general-tab.png)

35. Valitse **OK**, jotta voit sulkea **Käynnistä** -valintaikkunan ja palata **Kaikki tuotantotilaukset** -sivulle.

    Keräysluettelo luodaan materiaaleille, joita käytetään pinnoituksen työvaiheessa, ja palvelunimikkeelle. Palvelunimike edustaa alihankintana suoritettavan työvaiheen kustannuksia.

36. Valitse toimintoruudun **Näytä**-välilehdessä **Keräysluettelo**, jotta voit avata **Keräysluettelo**-sivun.
37. Valitse keräilylettelo, jota ei kirjata, ja valitse sitten kirjauskansion numero, jotta voit tarkastella kirjauskansion rivejä.

    ![Kirjauskansion rivit Keräysluettelo-sivulla](./media/subcontract25_picking-list.png)

38. Valitse toimintoruudussa **Tulosta**\>**Keräysluettelon raportti**, jotta voit avata **Keräysluettelon raportti** -valintaikkunan.
39. Määritä **Käytä toimitusilmoituksen asettelua** -vaihtoehdon arvoksi **Kyllä**.

    ![Keräysluettelon raportti -valintaikkuna](./media/subcontract26_picking-list-report-dialog.png)

40. Valitse **OK**, jotta voit luoda **Keräysluettelo**-raportin.

    Tässä tapauksessa toimittajan toimitusilmoitus tulostetaan tuotannon keräysluettelon kirjauskansiosta. Toimitusilmoituksessa määritetään materiaalit, jotka lähetetään toimittajalle, joka suorittaa pinnoituksen työvaiheen.

    ![Keräysluetteloraportti](./media/subcontract27_picking-list-report.png)

41. Sulje **Keräysluettelo**-raportti, jotta voit palata **Keräysluettelo**-sivulle.
42. Valitse toimintoruudussa **Kirjaus**, jotta voit avata **Kirjauskansio**-valintaikkunan.

    ![Kirjauskansio-valintaikkuna](./media/subcontract28_post-journal-dialog.png)

43. Valitse **OK**, jotta voit sulkea **Kirjauskansio**-valintaikkunan.
44. Avaa ostotilaus.

    ![Ostotilaus-sivu](./media/subcontract29_purchase-order-page.png)

45. Valitse toimintoruudun **Osto**-välilehdessä **Vahvista**.
46. Valitse **Kirjaus**, jotta voit avata **Kirjauskansio**-valintaikkunan.
47. Valitse **OK**, jotta voit sulkea **Kirjauskansio**-valintaikkunan ja palata **Ostotilaus**-sivulle.
48. Muuta yksikköhinta arvosta **33** arvoon **40**.

    ![Yksikköhinta muuttunut Ostotilaus-sivulla](./media/subcontract30_unit-price.png)

49. Vahvista ostotilaus uudelleen.
50. Tuotekuitti.

    ![Tuotekuitin kirjaus -valintaikkuna](./media/subcontract31_posting-product-receipt-dialog.png)

51. Ostolasku.
52. Päivitä täsmäytyksen tilaa.

    ![Toimittajalasku-sivu](./media/subcontract32_vendor-invoice-page.png)

53. Ilmoita valmiiksi.

    ![Ilmoita valmiiksi -valintaikkuna](./media/subcontract33_report-as-finished-dialog.png)

54. Loppu.

    ![Loppu-valintaikkuna](./media/subcontract34_end-dialog.png)

55. Kustannusvertailu.

    ![Kustannusvertailukaaviot](./media/subcontract35_cost-comparison-charts.png)

Puuttuva määritys tiedoissa.
