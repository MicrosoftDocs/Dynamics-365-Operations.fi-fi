---
title: Ruotsin Intrastat
description: Tässä artikkelissa on tietoja Intrastat-raportoinnista Ruotsissa.
author: AdamTrukawka
ms.date: 08/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: e13076a6b8f18374c012a5b56f13e752010256b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279228"
---
# <a name="swedish-intrastat"></a>Ruotsin Intrastat

[!include[banner](../includes/banner.md)]

**Intrastat**-sivun avulla voit luoda ja raportoida tietoja Euroopan unionin maiden/alueiden välisestä kaupasta. Ruotsin Intrastat-ilmoituksessa on raportoinnissa käytettäviä tietoja tavaroiden kaupasta.

Ruotsin Intrastat-ilmoituksessa on seuraavat kentät:

   - Kumppanimaan ISO-koodi
   - Tapahtumakoodi
   - Kauppatavarakoodi
   - Lisäyksikkö
   - Paino
   - Laskun summa

## <a name="set-up-intrastat"></a>Määritä Intrastat

Seuraavien sähköisen raportoinnin (ER) määritysten uusin versio on tuotava:

   - Intrastat-malli
   - Intrastat-raportti
   - Intrastat (SE)

Lisätietoja on kohdassa [ER-määritysten lataaminen määrityspalvelun yleisestä varastosta](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Määritä ulkomaankaupan parametrit

1. Valitse Microsoft Dynamics 365 Financessa **Vero** > **Määritys** > **Ulkomaankaupan parametrit**.
2. Valitse **Intrastat**-välilehden **Sähköinen raportointi** -pikavälilehden **Tiedostomuodon määritys** -kentässä **Intrastat (SE)**.
3. Valitse **Raporttimuodon määritys** -kentässä **Intrastat-raportti**.
4. Valitse **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kentästä **Intrastat**.
5. Valitse **Tapahtumakoodi**-kentässä ominaisuussiirtojen tapahtumakoodi. Tätä koodia käytetään tapahtumissa, jotka tuottavat toteutuneita tai suunniteltuja ominaisuussiirtoja (taloudellista tai muuta) kompensaatiota vastaan. Koodia käytetään myös korjauksiin. Ruotsin yrityksissä käytetään yksinumeroisia tapahtumakoodeja.
6. Valitse **Hyvityslasku**-kentässä tapahtumakoodi tavaroiden palautusta varten.
7. Ilmoita **Maan tai alueen ominaisuudet** -välilehden **Maa tai alue** -kentässä kaikki maat tai alueet, joiden kanssa yritys käy kauppaa. Valitse kullekin EU:n jäsenvaltion kohdalla **Maa-/aluetyyppi**-kentässä **EU**, minkä jälkeen maa näkyy Intrastat-raportissa.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>Intrastat-ilmoituksen tuoteparametrien määrittäminen

1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
2. Valitse tuote ruudukossa.
3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä kauppatavarakoodi.
4. Anna **Varastonhallinta**-pikavälilehden **Nettopaino**-kentässä tuotteen paino kilogrammoina.
5. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Intrastatin pakkaus** ja valitse sitten kentät, joita on vertailtava, kun Intrastat-tiedoista tehdään yhteenveto. Valitse Ruotsin Intrastat-raporttiin seuraavat kentät:

    - Kauppatavara
    - Tapahtumakoodi
    - Siirtosuunta
    - Maa tai alue
    - Korjaus
    - Lasku

## <a name="intrastat-transfer"></a>Intrastat-siirto

**Intrastat**-sivulla voit valita **Siirto**-kentässä automaattisesti siirrettäviksi yhteisön sisäistä kauppaa koskevat tiedot myyntitilauksesta, vapaatekstilaskuista, ostotilauksista, toimittajalaskuista, toimittajan tuotteen vastaanotoista, projektilaskuista ja siirtotilauksista. Vain ne asiakirjat siirretään, joissa on EU-maa tai -alue vastaanottajana (lähetyksille) tai vastaanottajana (saapuville).

Vaihtoehtoisesti voit syöttää tapahtumat manuaalisesti valitsemalla toimintoruudusta **Uusi**.

### <a name="generate-an-intrastat-report"></a>Luo Intrastat-raportti

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Tuloste** > **Raportti**.
3. Määritä seuraavat kentät **Intrastat-raportti**-valintaruudussa.

    | Kenttä            | kuvaus                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Päivämäärästä        | Valitse raportin aloituspäivä.                                                                                               |
    | Päivämäärään          | Valitse raportin päättymispäivä.                                                                                                 |
    | Luo tiedosto    | Luo Intrastat-raportin .txt-tiedosto valitsemalla tämän vaihtoehdon arvoksi **Kyllä**.                                                       |
    | Tiedostonimi        | Anna .txt-tiedoston nimi.                                                                                                    |
    | Luo raportti  | Luo Intrastat-raportin .xlsx-tiedosto valitsemalla tämän vaihtoehdon arvoksi **Kyllä**.                                                     |
    | Raporttitiedoston nimi | Anna .xlsx-tiedoston nimi.                                                                                                   |
    | Siirtosuunta        | Valitse **Saapumiset**, kun haluat raportin yhteisön sisäisistä saapumisista. Valitse **Lähetykset**, kun haluat raportin yhteisön sisäisistä lähetyksistä. |

4. Valitse **OK** ja tarkista luodut raportit.

## <a name="example"></a>Esimerkki

Tässä esimerkissä näytetään, miten tuonti ja vienti kirjataan Intrastat-raportointia varten. Se käyttää **DEMF**-yritystä.

### <a name="preliminary-setup"></a>Alustavat asetukset

1. Valitse **Organisaation hallinta** > **Organisaatio** > **Yritykset** ja valitse **DEMF**-yritys.
2. Valitse ensin **Osoite**-pikavälilehdessä **Muokkaa** ja valitse sitten **Maa tai alue** -kentässä **SWE (Ruotsi)**.
3. Seuraavien ER-määritysten uusin versio on tuotava:

    - Intrastat-malli
    - Intrastat-raportti
    - Intrastat (SE)

### <a name="create-transaction-codes"></a>Tapahtumakoodien luominen

1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Tapahtumakoodit**.
2. Valitse toimintoruudussa **Uusi**.
3. Anna **Tapahtuma****koodi**-kenttään **1**.
4. Anna **Nimi**-kentässä **Normaalit tapahtumat**.
5. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-foreign-trade-parameters"></a>Määritä ulkomaankaupan parametrit

1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Ulkomaankaupan parametrit**.
2. Valitse **Intrastat**-välilehden **Yleiset**-pikavälilehden **Tapahtuma****koodi**-kentässä **1**.
3. Valitse **Sähköinen raportointi** -pikavälilehden **Tiedostomuodon määritys** -kentässä **Intrastat (SE)**.
4. Valitse **Raporttimuodon yhdistäminen** -kentässä **Intrastat-raportti**.
5. Varmista, että **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kentässä on valittu **Intrastat**.
6. Valitse **Maan tai alueen ominaisuudet** -välilehdessä **Uusi**.
7. Valitse **Osapuolen maa/alue**-kentässä **SWE**.
8. Valitse **Maa-/aluetyyppi**-kentässä **Kotimaa**.
9. Valitse **Osapuolen maa tai alue** -kentässä **DEU** ja valitse sitten **Maa-/aluetyyppi**-kentässä **EU**.

### <a name="set-up-product-information"></a>Tuotetietojen määrittäminen

1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
2. Valitse ruudukossa **D0001**.
3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä **100 200 30**.
4. Anna **Nettopaino**-kentässä **5** **Varastonhallinta**-pikavälilehden **Painomitat**-osassa.
5. Valitse toimintoruudussa **Tallenna**.

### <a name="change-the-site-address"></a>Toimipaikan osoitteen muuttaminen

1. Valitse **Varastonhallinta** > **Asetukset** > **Varasto** > **Toimipaikat**.
2. Valitse ruudukossa **1**.
3. Valitse **Osoitteet**-pikavälilehdessä **Muokkaa**.
4. Valitse **Muokkaa osoitetta** -valintaikkunan **Maa tai alue** -kentässä **SWE**.
5. Valitse **OK**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>EU-asiakkaan myyntitilauksen luominen

1. Valitse **Myyntireskontra** > **Tilaukset** > **Kaikki myyntitilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Luo myynti tilaus** -valintaikkunan **Asiakas**-pikavälilehden **Asiakas**-osan **Asiakastili**-kentässä **DE-015**.
4. Valitse **Yleiset**-pikavälilehden **Varastodimensiot**-osan **Toimipaikka**-kentässä **1**.
5. Valitse **Varasto**-kentässä **11**.
6. Valitse **OK**.
7. Valitse **Rivit**-välilehden **Myyntitilauksen rivit** -pikavälilehden **Nimikkeen numero** -kentässä **D0001**. Anna sitten **Määrä**-kenttään **10**.
8. Varmista **Rivin erittely** -pikavälilehden **Ulkomaankauppa**-välilehdessä, että **Tapahtuma koodi**- ja **Kauppatavara**-kentät on määritetty automaattisesti.
9. Valitse toimintoruudussa **Tallenna**.
10. Valitse toimintoruudun **Lasku**-välilehden **Luo**-osassa **Lasku**.
11. Valitse **Laskun kirjaus**-valintaikkunan **Parametrit**-pikavälilehden **Parametri**-osan **Määrä**-kentästä **Kaikki**.
12. Kirjaa lasku valitsemalla **OK**.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Tapahtuman siirtäminen Intrastat-kirjauskansioon ja tuloksen tarkistaminen

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Siirto**.
3. Määritä **Intrastat (Siirto)** -valintaikkunan **Parametrit**-osassa **Myyntilasku**-asetuksen arvoksi **Kyllä**.
4. Valitse **Suodata**.
5. Valitse **Intrastat-suodatin**-valintaikkunan **Alue**-välilehdessä ensimmäinen rivi ja varmista, että **Kenttä**-kentän arvo on **Päivämäärä**.
6. Valitse **Ehdot**-kentässä kuluva päivä.
7. Sulje **Intrastat-suodatin**-valintaikkuna valitsemalla **OK**.
8. Sulje **Intrastat (siirto)** -valintaikkuna valitsemalla **OK** ja tarkista tulos. Rivi ilmaisee aiemmin luodun myyntitilauksen.

    ![Myyntitilauksen Intrastat-kirjauskansion rivit](media/swe_intrastat_journal_sales_order.png)

9. Saat lisätietoja valitsemalla ensin tapahtumarivin ja sitten **Yleiset**-välilehden.

    ![Myyntitilauksen Intrastat-kirjauskansion rivin erittely](media/swe_intrastat_journal_sales_order_line_details.png)

10. Valitse toimintoruudussa **Tuloste** > **Raportti**.
11. Valitse **Intrastat-raportin** valintaikkunan **Parametrit**-pikavälilehden **Päivämäärä**-osasta luomasi myyntitilauksen kuukausi.
12. Määritä **Vientiasetukset**-osassa **Muodosta** **tiedosto** -asetuksen arvoksi **Kyllä**. Anna sitten **Tiedostonimi**-kenttään tarvittava nimi.
13. Määritä **Luo raportti** -asetukseksi **Kyllä**. Anna sitten **Raporttitiedoston nimi** -kenttään tarvittava nimi.
14. Valitse **Suunta**-kentässä **Vienti**.
15. Valitse **OK** ja tarkista luotu .txt-muotoinen raportti. Seuraavassa taulukossa on esimerkkiraportin arvot.

    | Kumppanimaan ISO-koodi | Tapahtumakoodi | Kauppatavarakoodi | Lisäyksikkö | Paino | Laskun summa |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | VS                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Tarkista luotu Excel-muotoinen raportti.

    ![Intrastat-raportti](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Ostotilauksen luominen

1. Valitse **Ostoreskontra** > **Ostotilaukset** > **Kaikki ostotilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Luo ostotilaus** -valintaikkunan **Toimittajatili**-kentässä **DE-001**.
4. Valitse **OK**.
5. Tarkista **Otsikko**-välilehden **Ulkomaan****kauppa**-pikavälilehdessä, että **Tapahtumakoodi**-kentän määrityksenä on **1**.
6. Valitse **Rivit**-välilehden **Ostotilauksen rivit** -pikavälilehden **Nimikkeen numero** -kentässä **D0001**. Anna sitten **Määrä**-kenttään **6**.
7. Valitse toimintoruudun **Ostot**-välilehden **Toiminnot**-ryhmässä **Vahvista**.
8. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
9. Valitse toimintoruudussa **Oletusarvo kohteesta**. Valitse **Rivien oletusmäärä** -kentässä **Tilattu määrä**. Valitse sitten **OK**.
10. Anna **Toimittajan laskun otsikko** -pikavälilehden **Laskun tunnus** -osan **Numero**-kentässä **0001**.
11. Kirjaa lasku valitsemalla toimintoruudussa **Kirjaa**.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Tuonnin Intrastat-ilmoituksen luominen

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Siirto**.
3. Määritä **Intrastat (Siirto)** -valintaikkunan **Toimittajan lasku**-asetukseksi **Kyllä**.
4. Siirrä tapahtumat valitsemalla **OK** ja tarkista Intrastat-kirjauskansio.

    ![Ostotilauksen Intrastat-kirjauskansio](media/swe_intrastat_journal_purchase_order.png)

5. Tarkista ostotilauksen **Yleiset**-välilehti.

    ![Ostotilauksen Intrastat-kirjauskansion rivin erittely](media/swe_intrastat_journal_purchase_order_line_details.png)

6. Valitse toimintoruudussa **Tuloste** > **Raportti**.
7. Valitse **Intrastat-raportin** valintaikkunan **Parametrit**-pikavälilehden **Päivämäärä**-osasta luomasi myyntitilauksen kuukausi.
8. Määritä **Vientiasetukset**-osassa **Muodosta** **tiedosto** -asetuksen arvoksi **Kyllä**. Anna sitten **Tiedostonimi**-kenttään tarvittava nimi.
9. Määritä **Luo raportti** -asetukseksi **Kyllä**. Anna sitten **Raporttitiedoston nimi** -kenttään tarvittava nimi.
10. Valitse **Suunta**-kentässä **Tuonti**.
11. Valitse **OK** ja tarkista luotu .txt-muotoinen raportti. Seuraavassa taulukossa on esimerkkiraportin arvot.

    | Kumppanimaan ISO-koodi | Tapahtumakoodi | Kauppatavarakoodi | Lisäyksikkö | Paino | Laskun summa |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | VS                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Tarkista luotu Excel-muotoinen raportti.

    ![Tuonnin Intrastat-raportti](media/swe_intrastat_arrivals_report.png)
