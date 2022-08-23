---
title: Saksan Intrastat
description: Tässä artikkelissa on tietoja Saksan Intrastat-ilmoituksesta.
author: AdamTrukawka
ms.date: 09/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: ae978b28098d92d84415c29bbe76157144f862d8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269431"
---
# <a name="german-intrastat"></a>Saksan Intrastat

[!include [banner](../includes/banner.md)]

**Intrastat**-sivun avulla voit luoda ja raportoida tietoja Euroopan unionin maiden/alueiden välisestä kaupasta. Saksan Intrastat-ilmoituksessa on raportoinnissa käytettäviä tietoja tavaroiden kaupasta. Raportin muotoilussa käytetään Saksan viranomaisten ohjeita, jotka esitetään [6.2 Tiedostomäärittelyt INSTAT/XML-muodossa](https://www-idev.destatis.de/idev/doc/intra_en/hilfe6_2.html) -sivulla.

Seuraavassa taulukossa näkyvät Saksan Intrastat-ilmoitukseen sisältyvät kentät.

| Kentät | Toimitukset | Saapumiset |
|-------------------------|-------------------------|-------------------------|
| Viitekausi | X | X |
| Suuntakoodi | X | X |
| Intrastat-ilmoituksen valuutta</br>**Huomautus:** tämä valuutta on <em>kirjanpitovaluutta</em>. | X | X |
| Kauppatavarakoodi | X | X |
| Kauppatavaran nimi | X | X |
| Paljousyksikön koodi | X | X |
| Lähetys- tai määrämaa | X | X |
| Nettopaino | X | X |
| Määrä toisena paljoutena | X | X |
| Alkuperämaa/-alue |  | X |
| Laskun summa | X |  |
| Tilastollinen arvo | X | X |
| Kauppatapahtuman luonne | X | X |
| Kuljetusmuoto | X | X |
| Aluekoodi</br>**Huomautus:**</br><ul></br><li>Jos alkuperämaa tai -alue on Saksa ja lasku on viennille, alkuperämaan Intrastat-koodi näytetään.</li></br><li>Jos alkuperämaa tai -alue ei ole Saksa ja lasku on viennille, näkyvissä on koodi **99**.</li></br><li>Jos lasku on tuonnille, näkyvissä on maa Intrastat-koodi.</li></br></ul> | X | X |
| Satama-/lentoasema-/sisävesisatamakoodi | X | X |
| Toimitusehdot | X | X |


## <a name="set-up-intrastat"></a>Määritä Intrastat

1. Määritä yrityksen koodit.

    1. Valitse **Organisaation hallinto** > **Organisaatiot** > **Yritykset**.
    2. Anna **Ulkomaankauppa ja logistiikka** -pikavälilehden **Tunnus**-osan **DVR**-kentässä yhteiskäyttöä koskevan sopimuksen tunnus. Tämä tunnus sisällytetään raporttiin.
    3. Anna **ALV-tunnuksen vienti** -kenttään yrityksen viennin arvonlisäverotunnus (ALV-tunnus).
    4. Anna **ALV-tunnuksen tuonti** -kenttään yrityksen tuonnin arvonlisäverotunnus (ALV-tunnus).
    5. Anna **Intrastat-koodi**-kenttään yritykselle määritetty Intrastat-koodi.
    6. Syötä yrityksesi verorekisteröintinumero **Verorekisteröinti**-pikavälilehden **Verorekisteröintinumero**-kenttään.

    > [!NOTE]
    > Jos Intrastat-raportti luodaan osakkuusyrityksille, anna **Verorekisterinumero**-kenttään pääyrityksen verorekisterinumero.

2. Lataa [Microsoft Dynamics Lifecycle Servicesin (LCS)](https://lcs.dynamics.com/Logon/Index) jaetussa omaisuuskirjastossa seuraavan Intrastat-ilmoituksen uusimmat sähköisen raportoinnin (ER) määritykset.

    - Intrastat-malli
    - Intrastat-raportti
    - INSTAT XML
    - INSTAT XML (DE)

3. Määritä ulkomaankaupan parametrit.

    1. Siirry Dynamics 365 Financessa kohtaan **Vero** > **Asetukset** > **Ulkomaankaupan parametrit**.
    2. Valitse **Intrastat**-välilehden **Sähköinen raportointi** -pikavälilehden **Tiedostomuodon määritys** -kentässä **Intrastat XML (DE)**.
    3. Valitse **Raporttimuodon määritys** -kentässä **Intrastat-raportti**.
    4. Valitse **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kentästä **Intrastat**.
    5. Valitse **Tapahtumakoodi**-kentässä ominaisuussiirtojen tapahtumakoodi. Tätä koodia käytetään tapahtumissa, jotka tuottavat toteutuneita tai suunniteltuja ominaisuussiirtoja (taloudellista tai muuta) kompensaatiota vastaan. Koodia käytetään myös korjauksiin.
    6. Valitse **Hyvityslasku**-kentässä tapahtumakoodi tavaroiden palautusta varten.
    7. Valitse **Työntekijä**-kentässä yhteyshenkilö Intrastat-raporttia varten. Vaihtoehtoisesti voit syöttää tai valita arvoja **Yhteyshenkilö**-välilehden kentissä **Nimi**, **Puhelinnumero**, **Faksi**, **Sähköposti** ja **Internet-osoite**. Nämä kentät sisältyvät raporttiin.
    8. Valitse **Viranomainen**-kentässä viranomaiseksi Intrastat.
    9. Valitse **Vero** > **Välilliset verot** > **Arvonlisävero** > **Alv-viranomaiset** ja anna seuraavat edellisessä vaiheessa valittua Intrastat-viranomaista koskevat tiedot:

       - Viranomaisen tunnus
       - Osoite
       - Yhteystiedot

    10. Ilmoita **Maan tai alueen ominaisuudet** -välilehden **Maa tai alue** -kentässä kaikki maat tai alueet, joiden kanssa yritys käy kauppaa. Valitse kunkin tai alueen **Maa-/aluetyyppi**-kentässä **EU**, minkä jälkeen maa tai alue näkyy Intrastat-raportissa.

4. Määritä aluekoodit.

    1. Valitse **Organisaation hallinto** > **Yleinen osoitekirja** > **Osoitteet** > **Osoitemääritys**.
    2. Valitse **Osavaltio tai provinssi** -välilehden **Maa tai alue** -kentässä **DEU** ja valitse sitten **Käytä suodatinta**.
    3. Valitse ruudukossa osavaltio. Anna sitten **Intrastat-koodi**-kenttään yksilöivä Intrastat-koodi.

5. Määritä tuotteen alkuperän osoite.

    1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
    2. Valitse tuote ruudukossa.
    3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Alkuperämaa**-kentässä **DEU**.

6. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Intrastatin pakkaus** ja valitse sitten kentät, joita on vertailtava, kun Intrastat-tiedoista tehdään yhteenveto. Valitse Saksan Intrastat-raporttiin seuraavat kentät:

    - Kauppatavara
    - Maa tai alue
    - Korjaus
    - Siirtosuunta
    - Toimitusehdot
    - Lasku
    - Alkuperämaa/-alue
    - Portti
    - Lähettäjän maa tai alue
    - Lähettäjän osavaltio
    - Tilastomenettely
    - Tapahtumakoodi
    - Välitys
    - ALV-tunnus

### <a name="intrastat-transfer"></a>Intrastat-siirto

Kun **Intrastat**-sivun toimintoruudussa valitaan **Siirto**, yhteisön sisäistä kauppaa koskevat tiedot myyntitilauksesta, vapaatekstilaskuista, ostotilauksista, toimittajalaskuista, toimittajan tuotteen vastaanotoista **,** projektilaskuista ja siirtotilauksista siirretään automaattisesti. Vain ne asiakirjat siirretään, joissa on EU-maa tai -alue vastaanottajana (lähetyksille) tai vastaanottajana (saapuville).

Vaihtoehtoisesti voit syöttää tapahtumat manuaalisesti valitsemalla toimintoruudusta **Uusi**.

### <a name="generate-an-intrastat-report"></a>Luo Intrastat-raportti

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Tuloste** > **Raportti**.
3. Määritä seuraavat kentät **Intrastat-raportti**-valintaruudussa.

    | Kenttä | kuvaus |
    |-------------------------|-------------------------|
    | Päivämäärästä | Valitse raportin aloituspäivä. |
    | Päivämäärään | Valitse raportin päättymispäivä. |
    | Luo tiedosto | Määritä tämän vaihtoehdon arvoksi **Kyllä**, jos haluat luoda .xml-tiedoston. |
    | Tiedostonimi | Jätä tämä kenttä tyhjäksi. Tiedostonimi luodaan automaattisesti, ja se koostuu **&lt;envelopeId&gt;**-XML-tunnisteen arvosta sekä tiedostotunnisteesta **.xml**.</br>**&lt;envelopeId&gt;**-arvo muodostuu seuraavista, seuraavassa järjestyksessä ketjutetuista elementeistä:</br><ol type="1"></br><li>**&lt;interchangeAgreementId&gt;**-tunnisteen arvo</li></br><li>Tavuviiva (-)</li></br><li>**&lt;referencePeriod muodossa VVVVKK&gt;**-tunnisteen arvo</li></br><li>Tavuviiva (-)</li></br><li>**&lt;Envelope/DateTime/päivämäärä muodossa VVVVKKPP&gt;**-tunnisteen arvo</li></br><li>Tavuviiva (-)</li></br><li>**&lt;Envelope/DateTime/aika muodossa hhmm&gt;**-tunnisteen arvo</li></br></ol> |
    | Siirtosuunta | <ul></br><li>Valitse **Saapumiset**, kun raportti koskee yhteisön sisäistä tuontia.</li></br><li>Valitse **Lähtevät**, kun raportti koskee yhteisön sisäistä vientiä.</li></br><li>Valitse **Molemmat**, kun raportti koskee sekä tuontia että vientiä.</li></br></ul> |
    | Verorekisterinumero | Anna rekisterinumero, jolla luodaan lähettäjän tunnuskoodi, jos numero ei ole sama kuin yrityksen verorekisterinumero. |


## <a name="example"></a>Esimerkki

Tässä esimerkissä näytetään, miten tuonti ja vienti kirjataan Intrastat-raportointia varten. Se käyttää **DEMF**-yritystä.

1. Lataa [LCS:n](https://lcs.dynamics.com/Logon/Index) jaetussa resurssikirjastossa viimeisimmät versiot seuraavista elektronisen raportoinnin (ER) määrityksistä Intrastat-ilmoituksen muodolle:

    - Intrastat-malli
    - Intrastat-raportti
    - Intrastat XML
    - Intrastat XML (DE)

2. Luo tapahtumakoodit.

    1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Tapahtumakoodit**.
    2. Valitse toimintoruudussa **Uusi**.
    3. Anna **Tapahtuma****koodi**-kenttään **21**.
    4. Anna **Nimi**-kenttään **Tavaroiden palautus**.
    5. Valitse toimintoruudussa **Tallenna**.

3. Määritä viranomaisen tunnusnumero.

    1. Valitse **Vero** > **Välilliset verot** > **Arvonlisävero** > **Alv-viranomaiset**.
    2. Valitse luettelossa **TA**.
    3. Anna **Viranomaisen tunnus** -kenttään **123**.

4. Määritä aluekoodit.

    1. Valitse **Organisaation hallinto** > **Yleinen osoitekirja** > **Osoitteet** > **Osoitemääritys**.
    2. Valitse **Osavaltio tai provinssi** -välilehden **Maa tai alue** -kentässä **DEU** ja valitse sitten **Käytä suodatinta**.
    3. Valitse ruudukossa **BE** ja anna sitten **Intrastat-koodi**-kenttään **11**.
    4. Valitse toimintoruudussa **Tallenna**.

5. Määritä ulkomaankaupan parametrit.

    1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Ulkomaankaupan parametrit**.
    2. Valitse **Intrastat**-välilehden **Yleiset**-pikavälilehden **Tapahtuma****koodi**-kentässä **11**.
    3. Valitse **Hyvityslasku**-kentässä **21**.
    4. Valitse **Viranomainen**-kentässä **TA**.
    5. Valitse **Sähköisen raportoinnin** pikavälilehden **Tiedostomuodon määritys** -kentästä **INSTAT XML (DE)**.
    6. Valitse **Raporttimuodon yhdistäminen** -kentässä **Intrastat-raportti**.
    7. Varmista, että **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kentässä on valittu **Intrastat**.
    8. Valitse **Maan tai alueen ominaisuudet** -välilehdessä **Uusi**.
    9. Valitse **Osapuolen maa/alue**-kentässä **FRA**.
    10. Valitse **Maa-/aluetyyppi**-kentässä **EU**.

6. Määritä tuotteelle kauppatavarakoodi ja määritä tuotteen alkuperä. **Kauppatavarakoodi**-, **Alkuperämaa tai -alue**- ja **Alkuperäosavaltio**-kentät määritetään sitten automaattisesti myynti- ja ostotilauksiin, kun tuote valitaan.

    1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
    2. Valitse ruudukossa **D0001**.
    3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä **920 20 34**.
    4. Valitse **Alkuperä**-osan **Maa tai alue** -kentässä **DEU**.
    5. Anna **Nettopaino**-kentässä **12** **Varastonhallinta**-pikavälilehden **Painomitat**-osassa.
    6. Valitse toimintoruudussa **Tallenna**.

7. Määritä toimitustavaksi kuljetus. Kuljetuskoodi määritetään sitten tilauksille automaattisesti, kun toimitustapa valitaan.

    1. Valitse **Hankinta** > **Määritys** > **Jakelu** > **Toimitustavat**.
    2. Valitse luettelossa **10**.
    3. Valitse **Ulkomaankauppa**-pikavälilehden **Kuljetus** -kentässä **01**.

8. Luo myyntitilaus EU-asiakkaalle.

    1. Valitse **Myyntireskontra** > **Tilaukset** > **Kaikki myyntitilaukset**.
    2. Valitse toimintoruudussa **Uusi**.
    3. Valitse **Luo myynti tilaus** -valintaikkunan **Asiakas**-pikavälilehden **Asiakas**-osan **Asiakastili**-kentässä **DE-012**.
    4. Valitse **Yleiset**-pikavälilehden **Varastodimensiot**-osan **Toimipaikka**-kentässä **1**.
    5. Valitse **Varasto**-kentässä **11**.
    6. Valitse **OK**.
    7. Valitse **Otsikko**-välilehden **Ulkomaankauppa**-pikavälilehden **Satama**-kentässä **53**.
    8. Valitse **Tilastomenettely**-kentässä **31710**.
    9.  Valitse **Rivit**-välilehden **Myynti tilauksen** **rivit** -pikavälilehden **Nimikkeen numero** -kentässä **D0001**. Anna sitten **Määrä**-kenttään **10**.
    10. Varmista **Ulkomaankauppa**-välilehden **Rivin erittely** -pikavälilehdessä, että **Tapahtuma koodi**-, **Kuljetus**-, **Kauppatavara**- ja **Alkuperämaa tai -alue** -kentät on määritetty automaattisesti.
    11. Valitse toimintoruudussa **Tallenna**.
    12. Valitse toimintoruudun **Lasku**-välilehden **Luo**-osassa **Lasku**.
    13. Valitse **Laskun kirjaus**-valintaikkunan **Parametrit**-pikavälilehden **Parametri**-osan **Määrä**-kentästä **Kaikki**.
    14. Kirjaa lasku valitsemalla **OK**.

9.  Siirrä tapahtuma Intrastat-kirjauskansioon ja tarkista tulos.

    1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
    2. Valitse toimintoruudussa **Siirto**.
    3. Määritä **Intrastat (Siirto)** -valintaikkunan **Parametrit**-osassa **Myyntilasku**-asetuksen arvoksi **Kyllä**.
    4. Valitse **Suodata**.
    5. Valitse **Intrastat-suodatin**-valintaikkunan **Alue**-välilehdessä ensimmäinen rivi ja varmista, että **Kenttä**-kentän arvo on **Päivämäärä**.
    6. Valitse **Ehdot**-kentässä kuluva päivä.
    7. Sulje **Intrastat-suodatin**-valintaikkuna valitsemalla **OK**.
    8. Sulje **Intrastat (siirto)** -valintaikkuna valitsemalla **OK** ja tarkista tulos. Rivi ilmaisee aiemmin luodun myyntitilauksen.

        ![Intrastat-sivulla olevan myyntitilauksen ilmaiseva rivi](media/intrastat_deu_1.png)

10. Saat lisätietoja valitsemalla ensin tapahtumarivin ja sitten **Yleiset**-välilehden.

    ![Myyntitilauksen tiedot Intrastat-sivun Yleiset-välilehdessä](media/intrastat_deu_2.png)

11. Luo hyvityslasku myyntitilauksen avulla.

    1. Valitse **Myyntireskontra** > **Tilaukset** > **Kaikki myyntitilaukset**.
    2. Valitse toimintoruudussa **Uusi**.
    3. Valitse **Luo myynti tilaus** -valintaikkunan **Asiakas**-pikavälilehden **Asiakas**-osan **Asiakastili**-kentässä **DE-012**.
    4. Valitse **Yleiset**-pikavälilehden **Varastodimensiot**-osan **Toimipaikka**-kentässä **1**.
    5. Valitse **Varasto**-kentässä **11**.
    6. Valitse **Otsikko**-välilehden **Ulkomaankauppa**-pikavälilehden **Satama**-kentässä **53**.
    7. Valitse **Tilastomenettely**-kentässä **31710**.
    8. Valitse **Rivit**-välilehden **Myynti tilauksen** **rivit** -pikavälilehden **Nimikkeen numero** -kentässä **D0001**. Anna sitten **Määrä**-kenttään **-2**.
    9. Valitse **Ulkomaankauppa**-välilehden **Rivin erittely** -pikavälilehden **Tapahtumakoodi**-kentässä **21**.
    10. Varmista, että **Kuljetus**-, **Kauppatavara**- ja **Alkuperämaa tai -alue** -kentät on määritetty automaattisesti.
    11. Valitse toimintoruudussa **Tallenna**.
    12. Valitse toimintoruudun **Lasku**-välilehden **Luo**-osassa **Lasku**.
    13. Valitse **Laskun kirjaus**-valintaikkunan **Parametrit**-pikavälilehden **Parametri**-osan **Määrä**-kentästä **Kaikki**.
    14. Kirjaa lasku valitsemalla **OK**.

12. Siirrä tapahtuma Intrastat-kirjauskansioon ja tarkista tulos.

    1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
    2. Valitse toimintoruudussa **Siirto**.
    3. Määritä **Intrastat (Siirto)** -valintaikkunan **Parametrit**-osassa **Myyntilasku**-asetuksen arvoksi **Kyllä**.
    4. Sulje **Intrastat (siirto)** -valintaikkuna valitsemalla **OK** ja tarkista tulos. Uusi rivi, jossa **Siirtosuunta**-kentän arvona **Saapumiset**, on lisätty.            
        Tämä rivi ilmaisee tavaroiden fyysisen palautuksen.

        ![Tavaroiden fyysisen palautuksen ilmaiseva rivi Intrastat-sivulla](media/intrastat_deu_3.png)

13. Saat lisätietoja valitsemalla ensin tapahtumarivin ja sitten **Yleiset**-välilehden.

    ![Tavaroiden fyysisen palautuksen tiedot Intrastat-sivun Yleiset-välilehdessä](media/intrastat_deu_4.png)

14. Luo korjaus myyntitilauksen avulla.

    1. Valitse **Myyntireskontra** > **Tilaukset** > **Kaikki myyntitilaukset**.
    2. Valitse toimintoruudussa **Uusi**.
    3. Valitse **Luo myynti tilaus** -valintaikkunan **Asiakas**-pikavälilehden **Asiakas**-osan **Asiakastili**-kentässä **DE-012**.
    4. Valitse **Yleiset**-pikavälilehden **Varastodimensiot**-osan **Toimipaikka**-kentässä **1**.
    5. Valitse **Varasto**-kentässä **11**.
    6. Valitse **Otsikko**-välilehden **Ulkomaankauppa**-pikavälilehden **Satama**-kentässä **53**.
    7. Valitse **Tilastomenettely**-kentässä **31710**.
    8. Valitse **Rivit**-välilehden **Myynti tilauksen** **rivit** -pikavälilehden **Nimikkeen numero** -kentässä **D0001**. Anna sitten **Määrä**-kenttään **-3**.
    9. Valitse **Ulkomaankauppa**-välilehden **Rivin erittely** -pikavälilehden **Tapahtumakoodi**-kentässä **11**.
    10. Varmista, että **Kuljetus**-, **Kauppatavara**- ja **Alkuperämaa tai -alue** -kentät on määritetty automaattisesti.
    11. Valitse toimintoruudussa **Tallenna**.
    12. Varmista, että **Tapahtumakoodi**-kentän arvo on 11.
    13. Valitse toimintoruudun **Lasku**-välilehden **Luo**-osassa **Lasku**.
    14. Valitse **Laskun kirjaus**-valintaikkunan **Parametrit**-pikavälilehden **Parametri**-osan **Määrä**-kentästä **Kaikki**.
    15. Kirjaa lasku valitsemalla **OK**.

15. Siirrä tapahtuma Intrastat-kirjauskansioon ja tarkista tulos.

    1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
    2. Valitse toimintoruudussa **Siirto**.
    3. Määritä **Intrastat (Siirto)** -valintaikkunan **Parametrit**-osassa **Myyntilasku**-asetuksen arvoksi **Kyllä**.
    4. Sulje **Intrastat (siirto)** -valintaikkuna valitsemalla **OK** ja tarkista tulos. Uusi rivi, jossa **Korjaus**-sarakkeessa on valintamerkki, on lisätty.

        ![Korjauksen rivi Intrastat-sivulla](media/intrastat_deu_5.png)

16. Saat lisätietoja valitsemalla ensin tapahtumarivin ja sitten **Yleiset**-välilehden.

    ![Korjauksen tiedot Intrastat-sivun Yleiset-välilehdessä](media/intrastat_deu_6.png)

17. Valitse toimintoruudussa **Tuloste** > **Raportti**.
18. Valitse **Intrastat-raportin** valintaikkunan **Parametrit**-pikavälilehden **Päivämäärä**-osasta luomasi myyntitilauksen kuukausi.
19. Määritä **Vientiasetukset**-osassa **Muodosta** **tiedosto** -asetuksen arvoksi **Kyllä**.
20. Kirjoita **Tiedostonimi**-kenttään vaadittu nimi.
21. Valitse **OK** ja tarkista luotu raportti. Seuraavassa taulukossa on esimerkkiraportin arvot.

    | **Nimi**                  | **Myyntilasku**  |   **Korjaus**   | **Hyvityslasku** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | referencePeriod           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | flowCode                  | D                  | A                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | goodsDescription          | Kaiutin            | Kaiutin            | Kaiutin         |
    | MSConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netMass                   | 120                | -36                | 24              |
    | invoicedAmount            | 3290               | -987               | \-              |
    | StatisticalValue          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 01                 | 01                 | 01              |
    | regionCode                | 11                 | 11                 | 11              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |

