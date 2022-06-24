---
title: Saapumisten ja lähetysten kirjaaminen Intrastatiin
description: Tämän artikkelin esimerkki osoittaa, miten tuonti ja vienti kirjataan Intrastat-raportointia varten.
author: anasyash
ms.date: 8/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: aef20f0261e103be7fe231a7efb39751ab4d1151
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862961"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>Saapumisten ja lähetysten kirjaaminen Intrastatiin

[!include [banner](../includes/banner.md)]

Tämän artikkelin esimerkki osoittaa, miten tuonti ja vienti kirjataan Intrastat-raportointia varten. Tässä esimerkissä käytetään **ITCO**-yritystä.

## <a name="setup"></a>Luo perustiedot

1. Seuraavien sähköisen raportoinnin (ER) määritysten uusin versio on tuotava:

    - Intrastat-malli
    - Intrastat-raportti
    - Intrastat (IT)

    Lisätietoja on kohdassa [ER-määritysten lataaminen määrityspalvelun yleisestä varastosta](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. Määritä Microsoft Dynamics 365 Financessa seuraavat sarjat jatkuviksi: **Gene\_397**, **Acco\_16403**, **Gene\_407** ja **PUR\_EU**.

    1. Valitse **Organisaation hallinta** > **Numerosarjat** > **Numerosarjat**.
    2. Valitse ruudukossa jokin numerosarjakoodi.
    3. Valitse toimintoruudussa **Muokkaa**.
    4. Määritä **Jatkuva**-asetuksen arvoksi **Kyllä** **Määritys**-osan **Yleiset**-pikavälilehdessä.
    5. Valitse toimintoruudussa **Tallenna**.

3. Määritä varaston osoite.

    1. Valitse **Varastonhallinta** &gt; **Asetukset** &gt; **Varasto** &gt; **Varastot**.
    2. Valitse luettelossa varasto **11**.
    3. Valitse **Osoite**-pikavälilehdessä **Lisää**.
    4. Anna **Uusi** **osoite** -valintaikkunan **Nimi** **tai** **kuvaus** -kentässä **Pää**.
    5. Valitse **Maa tai alue** -kentässä **ITA (Italia)**.
    6. Valitse **Paikkakunta**-kentässä **Aprilia**.
    7. Valitse **OK**.

4. Määritä tapahtumakoodit.

    1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Tapahtumakoodit**.
    2. Valitse **Uusi** ja määritä omaisuuden siirtojen tapahtumakoodi.

        - Syötä **Tapahtumakoodi**-kenttään **1**.
        - Anna **Nimi**-kenttään **Omaisuuden siirto**.

    3. Valitse **Uusi** ja määritä palautusten tapahtumakoodi.

        - Anna **Tapahtumakoodi**-kenttään **2**.
        - Anna **Nimi**-kenttään **Tavaroiden palautus**.

5.  Määritä ulkomaankaupan parametrit.

    1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Ulkomaankaupan parametrit**.
    2. Valitse **Intrastat**-välilehden **Yleiset**-pikavälilehden **Tapahtumakoodi**-kentässä **1**.
    3. Valitse **Hyvityslasku**-kentässä **2**.
    4. Valitse **Myynnin raportointikausi** -kentässä **Kuukausi**.
    5. Valitse **Ostojen raportointikausi** -kentässä **Kuukausi**.
    6. Valitse **Sähköinen raportointi** -pikavälilehden **Tiedostomuodon määritys** -kentässä **Intrastat (IT)**.
    7. Valitse **Raportoinnin muodon yhdistäminen** -kentässä **Intrastat-raportti**.
    8. Valitse **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kentässä **Intrastat**.
    9. Määritä **Tilastollinen arvo** -pikavälilehdessä **Tilastotietojen tulostaminen ja vieminen** -asetuksen arvoksi **Kyllä**.
    10. Varmista **Maan tai alueen ominaisuudet** -välilehdessä, että seuraavat rivit ovat käytössä:

        | **Osapuolen maa/alue** | **Intrastat-koodi** | **Valuutta** | **Maa- tai aluetyyppi** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | VS                 | EUR          | Kotimaa                |
        | SMR                      | SM                 | EUR          | Erityinen kotimainen        |

    11. Luo seuraava rivi valitsemalla työkalurivillä **Uusi**.

        | **Osapuolen maa/alue** | **Intrastat-koodi** | **Valuutta** | **Maa- tai aluetyyppi** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | DKK          | EU                      |

6. Määritä ALV-tunnukset.

    1. Valitse **Vero** > **Määritys** > **Arvonlisävero** > **ALV-tunnukset**.
    2. Luo seuraavat rivit valitsemalla toimintoruudussa **Uusi**.

        | **Maa/alue** | **ALV-tunnus** | **Yrityksen nimi** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | UE-TOIMITTAJA        |
        | DNK                | DK0987654321          | Asiakkaan ER      |

7. Määritä toimittajan osoite.

    1. Siirry kohtaan **Ostoreskontra** &gt; **Toimittajat** &gt; **Kaikki toimittajat**.
    2. Valitse ruudukossa **UE-toimittaja**.
    3. Valitse **Osoitteet**-pikavälilehdessä **Lisää**.
    4. Anna **Uusi osoite**-valintaruudun **Nimi tai kuvaus** -kenttään **Saksa**.
    5. Valitse **Maa tai alue**-kentässä **DEU**.
    6. Luo uusi osoite valitsemalla **OK**.
    7. Valitse **Lasku ja toimitus** -pikavälilehden **Arvonlisävero**-osan **ALV-tunnus**-kentässä **Kaikki** ja valitse sitten **DE1234567890**.
    8. Valitse toimintoruudussa **Tallenna**.

8. Määritä asiakkaan osoitteet.

    1. Valitse **Myyntireskontra** > **Asiakkaat** > **Kaikki asiakkaat**.
    2. Valitse ruudukossa **ITCO-000001**.
    3. Valitse **Osoitteet**-pikavälilehdessä **Muokkaa**.
    4. Anna **Uusi osoite**-valintaruudun **Nimi tai kuvaus** -kenttään **San Marino**.
    5. Valitse **Maa tai alue**-kentässä **SMR**.
    6. Luo uusi osoite valitsemalla **OK**.
    7. Valitse **Lasku ja toimitus** -pikavälilehden **Lasku**-osan **Laskutustili**-kentässä **ITCO-000001**.
    8. Valitse **Numerosarjaryhmä**-kentässä **IT\_VENDOM**.
    9. Valitse toimintoruudussa **Tallenna** ja sulje sivu.
    10. Valitse ruudukon **Kaikki asiakkaat** -sivulla **ITCO-000002**.
    11. Valitse **Osoitteet**-pikavälilehdessä **Lisää**.
    12. Anna **Uusi osoite**-valintaruudun **Nimi tai kuvaus** -kenttään **Tanska**.
    13. Valitse **Maa tai alue**-kentässä **DNK**.
    14. Luo uusi osoite valitsemalla **OK**.
    15. Valitse **Myyntien demografia** -pikavälilehden **Valuutta**-kentässä **DKK**.
    16. Valitse **Lasku ja toimitus** -pikavälilehden **Arvonlisävero**-osan **Arvonlisäveroryhmä**-kentässä **IT\_PUREU**.
    17. Valitse **ALV-tunnus**-kentässä **Kaikki** ja valitse sitten **DK0987654321**.
    18. Valitse toimintoruudussa **Tallenna**.

9. Määritä luokkahierarkia.

    1. Valitse **Tuotetietojen hallinta** > **Määritys** > **Luokat ja määritteet** > **Luokkahierarkiat**.
    2. Valitse ruudukossa **Intrastat**.
    3. Valitse toimintoruudussa **Uusi luokkasolmu**.
    4. Anna **Nimi**-kentässä **Palvelu**.
    5. Anna **Koodi**-kentässä **123456**.
    6. Valitse toimintoruudussa **Tallenna**.

10. Määritä tuotteet.

    1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
    2. Valitse ruudukossa **ITEM**.
    3. Valitse **Ostot**-välilehden **Hallinta**-osan **Toimittaja**-kentässä **ITCO-000001**.
    4. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä **\[100 200 30\] Kaiutin**.
    5. Valitse **Alkuperä**-osan **Maa tai alue** -kentässä **DEU**.
    6. Valitse **Osavaltio tai provinssi** -kentässä **BE**.
    7. Anna **Varastonhallinta**-pikavälilehden **Nettomitat**-osan **Nettopaino**-kentässä **5**.
    8. Valitse toimintoruudussa **Tallenna**.
    9. Valitse ruudukon **Vapautetut tuotteet** -sivulla **Palvelunimike**.
    10. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä **\[123456\] Palvelu**.
    11. Valitse toimintoruudussa **Tallenna**.

11. Määritä kuljetustavat.

    1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Kuljetustapa**.
    2. Luo seuraavat kuljetustavat valitsemalla toimintoruudussa **Uusi**.

        | **Välitys** | **Kuvaus** |
        |---------------|-----------------|
        | 1             | Maantiekuljetus            |
        | 2             | Lentorahti             |

12. Määritä toimitustapa.

    1. Valitse **Hankinta** > **Määritys** > **Jakelu** > **Toimitustavat**.
    2. Valitse toimintoruudussa **Uusi**.
    3. Anna **Toimitustapa**-kentässä **1**.
    4. Anna **Kuvaus**-kentässä **Kuorma-auto**.
    5. Valitse **Ulkomaankauppa**-pikavälilehden **Kuljetus** -kentässä **1 Maantie**.
    6. Valitse toimintoruudussa **Tallenna**.

13. Määritä toimitusehdot.

    1. Valitse **Ostoreskontra** > **Määritys** > **Toimitusehdot**.
    2. Valitse luettelossa **CFR**.
    3. Anna **Yleinen**-pikavälilehden **Intrastat-koodi**-kentässä **1**.

## <a name="post-arrivals-for-intrastat"></a>Tuonnin kirjaaminen Intrastat-raportointia varten

### <a name="purchase-goods-by-using-a-purchase-order"></a>Tavaroiden ostaminen ostotilauksen avulla

Esimerkin tässä osassa näytetään, miten tavaroita (nimikkeitä) ostetaan Euroopan unionin (EU) jäsenmaista ostotilausta käyttämällä.

1. Valitse **Ostoreskontra** > **Ostotilaukset** > **Kaikki ostotilaukset**.
2.  Valitse toimintoruudussa **Uusi**.
3.  Valitse **Luo ostotilaus** -valintaikkunan **Toimittajatili**-kentässä **UE-toimittaja**.
4.  Valitse **Hallinta**-pikavälilehden **Kieli**-kentässä **it**.
5.  Valitse **OK**.
6.  Tarkista **Ulkomaankauppa**-pikavälilehden **Otsikko**-näkymässä, että **Tapahtumakoodi**-kentän määrityksenä on **1**.
7.  Tarkista, että **Alkuperä-/kohdemaa**-kentän määrityksenä on **RM**.
8.  Valitse **Toimitus**-pikavälilehden **Toimitus**-osan **Toimitustapa**-kentässä **1**.
9.  Valitse **Toimitusehdot**-kentässä **CFR**.
10. Valitse **Ostotilauksen rivit** -pikavälilehden **Rivit**-näkymän **Nimikkeen numero** -kentässä **Nimike**.
11. Valitse **Toimipaikka**-kentässä **1**.
12. Valitse **Varasto**-kentässä **11**.
13. Kirjoita **Määrä**-kenttään **10**.
14. Kirjoita **Yksikköhinta**-kentässä **100**.
15. Valitse **Määritys**-välilehden **Arvonlisävero**-osan **Nimikkeen arvonlisäveroryhmä**-kentässä **22%EU**.
16. Valitse toimintoruudun **Ostot**-välilehden **Toiminnot**-ryhmässä **Vahvista**.
17. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
18. Valitse toimintoruudussa **Oletusarvo kohteesta**.
19. Valitse **Rivien oletusmäärä** -kentässä **Tilattu määrä** ja valitse **OK**.
20. Anna **Toimittajan laskun otsikko** -pikavälilehden **Laskun tunnus** -osan **Numero**-kentässä **0001**.
21. Valitse **Laskujen päivämäärät** -osan **Laskun päivämäärä** -kentässä **9.7.2021**.
22. Kirjaa lasku valitsemalla toimintoruudussa **Kirjaa**.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Palvelujen ostaminen toimittajan laskun avulla

Esimerkin tässä osassa näytetään, miten palveluja ostetaan Euroopan unionin (EU) jäsenmaista toimittajan laskua käyttämällä.

1. Valitse **Ostoreskontra** > **Laskut** > **Laskun kirjauskansio**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Nimi**-kentässä **VEND\_EUINV**.
4. Valitse toimintoruudussa **Rivit**.
5. Anna **Päivämäärä**-kentässä **9.7.2021**.
6. Valitse **Tilityyppi**-kentässä **Toimittaja**.
7. Valitse **Tili**-kentässä **UE-toimittaja**.
8. Valitse **Laskun päivämäärä** -kentässä **9.7.2021**.
9. Anna **Lasku**-kentässä **ITA-0004**.
10. Anna **Hyvitys**-kentässä **120000**.
11. Valitse **Vastatilin** **tyyppi** -kentässä **Kirjanpito**.
12. Valitse **Vastatili**-kentässä **110130**.
13. Valitse **Arvonlisäveroryhmä**-kentässä **IT\_PUREU**.
14. Valitse **Nimikkeen arvonlisäveroryhmä** -kentässä **22%EU**.
15. Toimi seuraavasti **Ulkomaankauppa**-välilehdessä:

    1. Valitse **Tapahtumakoodi**-kentässä **1**.
    2. Valitse **Kuljetus**-kentässä **2 Lentorahti**.
    3. Valitse **Kauppatavara**-kentässä **\[123456\] Palvelu**.
    4. Valitse **Maa tai alue**-kentässä **ITA**.
    5. Valitse **Osavaltio tai provinssi** -kentässä **LAZ**.
    6. Valitse **Alkuperä-/kohdemaakunta**-kentässä **LT**.


16. Valitse toimintoruudussa **Kirjaa**.
17. Luo tuonnin Intrastat-ilmoitus.

    1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
    2. Valitse toimintoruudussa **Siirto**.
    3. Määritä **Intrastat (Siirto)** -valintaikkunan **Toimittajan lasku**-asetukseksi **Kyllä**.
    4. Siirrä tapahtumat valitsemalla **OK** ja tarkista sitten Intrastat-kirjauskansio.

   ![Intrastat-kirjauskansion sivu, Yhteenveto-välilehti.](media/ita_intrastat_journal_vendor_invoice.png)

18. Tarkista ostotilauksen **Yleiset**-välilehti.

    ![Ostotilauksen Intrastat-kirjauskansion rivin erittely](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Tarkista toimittajan laskun **Yleiset**-välilehti.

    ![Toimittajan laskun Intrastat-kirjauskansion rivin tiedot](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. Luo tuonnin Intrastat-raportti.

    1. Valitse toimintoruudussa **Tuloste** > **Raportti**.
    2. Valitse **Intrastat-raportti**-valintaikkunan **Päivämäärä**-osan **Alkamispäivä**-kentässä **1.7.2021**.
    3. Valitse **Päättymispäivä**-kentässä **31.7.2021**.
    4. Määritä **Vientiasetukset**-osassa **Muodosta tiedosto**- ja **Muodosta raportti** -asetusten arvoksi **Kyllä**.
    5. Anna **Tiedoston nimi** -kentässä **Tuonnin tiedosto**.
    6. Anna **Raporttitiedoston nimi** -kentässä **Tuonnin raportti**.
    7. Valitse **Suunta**-kentässä **Tuonti**.
    8. Anna **Viitenumero**-kentässä **123456**.
    9. Luo Intrastat-raportti ja Intrastat-tiedosto valitsemalla **OK** sekä tarkista ne.

    Seuraavassa kuvassa on esimerkki Intrastat-raportista.

    ![Tuonnin Intrastat-raportti](media/ita_intrastat_arrivals_report.png)

    Seuraavassa kuvassa on esimerkki Intrastat-tiedostosta.

    ![Tuonnin Intrastat-tiedosto](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>Viennin kirjaaminen Intrastat-raportointia varten

### <a name="sell-goods-by-using-a-sales-order"></a>Tavaroiden myynti myyntitilauksen avulla

Esimerkin tässä osassa näytetään, miten tavaroita (nimikkeitä) myydään Euroopan unionin (EU) jäsenmaihin myyntitilausta käyttämällä.

1. Valitse **Myyntireskontra** > **Tilaukset** > **Kaikki myyntitilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä **ITCO-000002**.
4. Valitse **OK**.
5. Valitse **Toimitus**-pikavälilehden **Otsikko**-näkymän **Muut toimitustiedot** -osan **Toimitustapa**-kentässä **1 Kuorma-auto**.
6. Valitse **Toimitusehdot**-kentässä **CFR**.
7. Valitse **Myyntitilauksen rivit** -pikavälilehden **Rivit**-näkymän **Nimikkeen numero** -kentässä **ITEM**.
8. Kirjoita **Määrä**-kenttään **50**.
9. Valitse **Toimipaikka**-kentässä **1**.
10. Valitse **Varasto**-kentässä **11**.
11. Kirjoita **Yksikköhinta**-kentässä **250**.
12. Valitse **Rivin tiedot** -pikavälilehden **Määritys**-välilehden **Arvonlisävero**-osan **Nimikkeen arvonlisäveroryhmä** -kentässä **22%EU**.
13. Valitse toimintoruudussa **Tallenna**.
14. Luo tilauksen lasku valitsemalla toimintoruudun **Lasku**-välilehden **Luo**-ryhmässä **Lasku**.
15. Valitse **Laskun kirjaus**-valintaikkunan **Parametrit**-pikavälilehden **Parametri**-osan **Määrä**-kentässä **Kaikki**.
16. Valitse **Määritys**-pikavälilehden **Laskun** **päivämäärä** -kentässä **9.7.2021**.
17. Valitse **OK**.
18. Tarkista Intrastat-kirjauskansion rivit.

    1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
    2. Valitse toimintoruudussa **Siirto**.
    3. Määritä **Intrastat (Siirto)** -valintaikkunan **Myyntilasku**-asetukseksi **Kyllä**.
    4. Siirrä tapahtumat valitsemalla **OK** ja tarkista Intrastat-kirjauskansio. Hyvityslaskutapahtuma merkitään korjaukseksi, ja laskun summa on negatiivinen.

        ![Intrastat-kirjauskansion sivu](media/ita_intrastat_journal_sales_order.png)

        ![Myyntitilauksen Intrastat-kirjauskansion rivin erittely](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Tavaroiden palauttaminen hyvityslaskun avulla

Esimerkin tässä osassa näytetään, miten tavaroita (nimikkeitä) palautetaan Euroopan unionin (EU) jäsenmaista hyvityslaskua käyttämällä.

1. Valitse **Myyntireskontra** > **Tilaukset** > **Kaikki myyntitilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä **ITCO-000002**.
4. Valitse **OK**.
5. Valitse **Toimitus**-pikavälilehden **Otsikko**-näkymän **Muut toimitustiedot** -osan **Toimitustapa**-kentässä **1 Kuorma-auto**.
6. Valitse **Toimitusehdot**-kentässä **CFR**.
7. Valitse **Ulkomaankauppa**-pikavälilehden **Tapahtumakoodi** -kentässä **2**.
8. Valitse **Rivit**-välilehden **Myyntitilauksen rivit** -pikavälilehden **Nimikkeen numero** -kentässä **ITEM**.
9. Anna **Määrä**-kentässä **-10**.
10. Valitse **Toimipaikka**-kentässä **1**.
11. Valitse **Varasto**-kentässä **11**.
12. Kirjoita **Yksikköhinta**-kentässä **250**.
13. Valitse **Rivin tiedot** -pikavälilehden **Määritys**-välilehden **Arvonlisävero**-osan **Nimikkeen arvonlisäveroryhmä** -kentässä **22%EU**.
14. Valitse **Palautettu tilaus** -osan **Palautuksen erätunnus** -kentässä aiemmin luotu erä.
15. Valitse toimintoruudussa **Tallenna**.
16. Luo tilauksen lasku valitsemalla toimintoruudun **Lasku**-välilehden **Luo**-ryhmässä **Lasku**.
17. Valitse **Parametrit**-pikavälilehden **Parametri**-osan **Määrä**-kentässä **Kaikki**.
18. Valitse **Laskun kirjaus** -valintaikkunan **Määritys**-pikavälilehden **Laskun** **päivämäärä** -kentässä **9.7.2021**.
19. Kirjaa lasku valitsemalla **OK**.
20. Tarkista Intrastat-kirjauskansion rivit.

    1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
    2. Valitse toimintoruudussa **Siirto**.
    3. Määritä **Intrastat (Siirto)** -valintaikkunan **Myyntilasku**-asetukseksi **Kyllä**.
    4. Siirrä tapahtumat valitsemalla **OK** ja tarkista Intrastat-kirjauskansio. Hyvityslaskutapahtuma merkitään korjaukseksi, ja laskun summa on negatiivinen.

    ![Intrastat-kirjauskansion hyvityslasku](media/ita_intrastat_journal_credit_note.png)

    ![Hyvityslaskun Intrastat-kirjauskansion rivin tiedot](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Tavaroiden myynti San Marinoon myyntitilauksen avulla

Esimerkin tässä osassa näytetään, miten tavaroita (nimikkeitä) ostetaan San Marinoon myyntitilausta käyttämällä.

1. Valitse **Myyntireskontra** > **Tilaukset** > **Kaikki myyntitilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä **ITCO-000001**.
4. Valitse **OK**.
5. Valitse **Toimitus**-pikavälilehden **Otsikko**-näkymän **Muut toimitustiedot** -osan **Toimitustapa**-kentässä **1**.
6. Valitse **Toimitusehdot**-kentässä **CFR**.
7. Valitse **Rivit**-välilehden **Myyntitilauksen rivit** -pikavälilehden **Nimikkeen numero** -kentässä **ITEM**.
8. Kirjoita **Määrä**-kenttään **30**.
9. Valitse **Toimipaikka**-kentässä **1**.
10. Valitse **Varasto**-kentässä **11**.
11. Kirjoita **Yksikköhinta**-kentässä **200**.
12. Valitse toimintoruudussa **Tallenna**.
13. Luo tilauksen lasku valitsemalla toimintoruudun **Lasku**-välilehden **Luo**-ryhmässä **Lasku**.
14. Valitse **Parametrit**-pikavälilehden **Parametri**-osan **Määrä**-kentässä **Kaikki**.
15. Valitse **Laskun kirjaus** -valintaikkunan **Määritys**-pikavälilehden **Laskun** **päivämäärä** -kentässä **9.7.2021**.
16. Kirjaa lasku valitsemalla **OK**.
17. Tarkista Intrastat-kirjauskansion rivit.

    1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
    2. Valitse toimintoruudussa **Siirto**.
    3. Määritä **Intrastat (Siirto)** -valintaikkunan **Myyntilasku**-asetukseksi **Kyllä**.
    4. Siirrä tapahtumat valitsemalla **OK** ja tarkista Intrastat-kirjauskansio.

   ![San Marinon Intrastat-kirjauskansio](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![San Marinon Intrastat-kirjauskansion rivin tiedot](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. Luo viennin Intrastat-ilmoitus.

    1. Siirry kohtaan **Vero** &gt; **Ilmoitukset** &gt; **Ulkomaankauppa** &gt; **Intrastat**.
    2. Valitse toimintoruudussa **Tuloste** &gt; **Raportti**.
    3. Valitse **Intrastat-raportti**-valintaikkunan **Päivämäärä**-osan **Alkamispäivä**-kentässä **1.7.2021**.
    4. Valitse **Päättymispäivä**-kentässä **31.7.2021**.
    5. Määritä **Vientiasetukset**-osassa **Muodosta tiedosto**- ja **Muodosta raportti** -asetusten arvoksi **Kyllä**.
    6. Anna **Tiedoston nimi** -kentässä **Viennin tiedosto**.
    7. Anna **Raporttitiedoston nimi** -kentässä **Viennin raportti**.
    8. Valitse **Suunta**-kentässä **Vienti**.
    9. Anna **Viitenumero**-kentässä **98754**.
    10. Luo Intrastat-raportti ja Intrastat-tiedosto valitsemalla **OK**.

        Seuraavassa kuvassa on esimerkki tulostetusta Intrastat-raportista.

        ![Intrastat-raportti](media/ita_intrastat_report_for_dispatches.png)

        Seuraavassa kuvassa on esimerkki tulostetusta Intrastat-tiedostosta.

        ![Viennin Intrastat-tiedosto](media/ita_intrastat_file_for_dispatches.png)
