---
title: Aallon etiketin tulostus
description: Tässä ohjeaiheessa käsitellään aallon etikettitulostusta ja sen määrittämistä.
author: perlynne
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 3040406af731e2e35fff456804f893108e7eb896bfa0132082986c09ad128952
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777668"
---
# <a name="wave-label-printing"></a>Aallon etiketin tulostus

[!include [banner](../includes/banner.md)]

Aallon etikettitulostus on vaihtoehtoinen tapa tulostaa etikettejä. Siinä otetaan käyttöön uusin aallon vaihe, jossa luodaan ja tulostetaan etikettejä suoraan aaltomallista aallon suorituksen aikana. Tämän vuoksi etiketit ovat saatavana jo ennen kuin työtekijät suorittavat työtilauksen mobiililaitteessa. Työntekijät voivat sitten kiinnittää tarvittavat etiketit keräilyn aikana eikä sen jälkeen.

Aallon etikettitulostus luo etikettiasettelut ZLP (Zebra Programming Language) -kielen avulla. Etikettiasettelu on jaettu kolmeen osaan (ylätunniste, teksti ja alatunniste), jolloin etikettien rakenne pysyy samana. Aallon etikettimalli ilmaisee järjestelmälle käytettävän etikettiasettelun. Käyttäjät voivat määrittää käytettävän tulostimen. He voivat myös tarvittaessa tulostaa etikettejä monessa tulostimessa samanaikaisesti. **Aallon etiketin historia** -sivulle on kirjattu kaikki etiketit, jotka on luotu kyseisellä määrityksellä.

Etikettejä voi tulostaa ja lajitella työn ylätunnisteiden perusteella, minkä lisäksi voidaan tulostaa työn ylätunnistekohtaisia keskeytysetikettejä sekä etikettejä kontin sisällöstä, laatikkoetikettejä ja muita vastaavia etikettejä.

> [!NOTE]
> Tämä toiminto ei korvaa nykyistä asiakirjan reititykseen perustuvaa etikettitulostustoimintoa.

Aallon etikettitulostukseen liittyvät parannukset:

- Etiketit tulostetaan yhden työrivin pakkausten määrän perusteella ilman konttiinpakkausta. (Pakkaus on yksikkö, joka on määritetty yksikön sarjaryhmäriveillä.)
- Useiden etikettisarjojen tulostaminen (kuten pakkaus- ja kuormalavaetiketit).
- Etiketin luetteloinnin (kuten 1/124, 2/124, ... 124/124) sisällyttäminen ja luettelointialueen määrittäminen (kuten työrivi, kuormarivi tai lähetys).
- Rahtikirjan tunnuksen luominen ja tulostaminen etiketteihin ennen rahtikirjan muodostamista.
- Yksilöivän SSCC (Serial Shipping Container Code) -koodiin luominen kullekin pakkaukselle ja sen sisällyttäminen jokaiseen tarraan.
- GS1-yhteensopivien numerosarjojen luominen rahtikirjan tunnuksille ja SSCC-koodeille.
- Etikettien uudelleentulostaminen sekä mobiililaitteita että raskaasta asiakkaasta.
- Etikettien mitätöinti (esimerkiksi lyhyissä keräilyskenaarioissa) ja niiden uudelleentulostaminen.
- Aallon etikettihistorian tyhjentäminen.
- Asiakirjareitityksen asettelujen parannukset jaetaan asiakirjareitityksen asettelujen ja aallon etiketin asettelujen kesken. (Lisätietoja on kohdassa [Rekisterikilven asiakirjareitityksen asettelu](../warehousing/document-routing-layout-for-license-plates.md).)

Nämä parannukset tehostavat etikettien käyttöä pakkauksissa ennen pakkausta kuormalavalle. Niistä on hyötyä etenkin suurille jälleenmyyjille lähettäville yrityksille, sillä ne vahvistavat tilausten vastaanotan lukemalla kunkin pakkauksen erikseen.

> [!NOTE]
> Tässä ohjeaiheessa käsiteltävät määritysskenaariot voidaan toteuttaa joko erikseen tai yhdistelminä sen mukaan, mikä vastaa parhaiten liiketoimintarpeita. Voit suunnitella useita aallon sarjana käytettäviä etikettimalleja (josta on esimerkki skenaariossa 3). Voit esimerkiksi käyttää skenaariota 1 pakkausten etikettien tulostamiseen ja skenaariota 2 kuormalavan etikettien tulostamiseen (jos varaston kuormalavojen koossa ja kokoonpanossa on eroja):

## <a name="turn-on-the-wave-label-printing-feature"></a>Aallon etiketin tulostustoiminnon ottaminen käyttöön

Ennen kuin voit käyttää *Aallon etikettitulostus* -toimintoa, sen on oltava otettuna käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Aallon etikettitulostus*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>Skenaario 1: Aallon etikettitulostus, kun luotavana on yksi aallon etiketti

Tässä skenaariossa näytetään, miten yritys voi tulostaa lähetyksen etikettejä suurelle jälleenmyyjälle, joka vahvistaa tilausten vastaanotot automaattisesti lukemalla kunkin pakkauksen erikseen.

Tämä skenaario sisältää työnkulun alusta loppuun.

### <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Tämän skenaarion käyttäminen edellyttää, että demotiedot on asennettu ja että **USMF**-yritys on valittu.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Aallon etikettimenetelmän saatavuuden varmistaminen

On mahdollista, että aallon käsittelymenetelmät on luotava uudelleen, jotta aallon etiketin tulostusmenetelmä on käytettävissä.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.
1. Varmista, että **waveLabelPrinting** on luettelossa. Jos se ei ole luettelossa, lisää se valitsemalla toimintoruudussa **Luo menetelmät uudelleen**.

### <a name="configure-a-wave-template"></a>Aaltomallin määrittäminen

Aaltomallin avulla tietyt aaltomenetelmien esiintymät voidaan linkittää vastaavaan aallon etikettimalliin.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Valitse malli, kuten **62 Lähetyksen oletus**.
1. Siirrä **Aallon etiketin tulostus** -menetelmä **Menetelmät**-pikavälilehdessä **Valitut menetelmät** -sarakkeeseen.
1. Valitse **Valitut menetelmät** -sarakkeessa **Aallon etiketin tulostus** -menetelmä ja valitsen sen **Aallon vaihekoodi** -kentässä *PrintLabel*. Lisätietoja aallon vaihekoodeista on kohdassa [Aallon vaihekoodit](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Aallon etikettiasettelun luominen

Etiketin asettelu määrittää, mitä tietoja etikettiin tulostetaan ja miten ne näkyvät etiketissä. Annettava ZPL-koodi lähetetään tulostimeen.

1. Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etiketin asettelut**.
1. Luo tietue, jossa on seuraavat asetukset:

    - **Etiketin asettelutunnus:** *Pakkaus*
    - **Kuvaus:** *Pakkaus (SSCC)*

1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Aallon etiketin riviasetukset**.

    **Aallon etiketin riviasetukset** -sivu avautuu. Etiketin dynaaminen osa määritetään tällä sivulla.

1. Lisää rivi, jossa on seuraavat asetukset:

    - **Rivin tunnus:** *WaveLabel*
    - **Rivin taulukon nimi:** *WHSWaveLabel*
    - **Rivin lähtökohta:** *0*

        Tämä kenttä määrittää pystysuunnassa paikan, josta rivi alkaa etiketissä.

    - **Rivin korkeus:** *0*

        Tämä kenttää määrittää kunkin rivin korkeuden (pisteinä) ZPL-standardin mukaisesti. Rivin korkeus on positiivinen vaakasuuntaisissa etiketeissä ja negatiivinen pystysuuntaisissa etiketeissä. Koska tässä esimerkissä on vain yksi rivi, arvoksi voidaan määrittää *0* (nolla).

    - **Riviä sivua kohden:** *1*

        Tämä kenttä määrittää, kuinka monta riviä kuhunkin etikettiin tulostetaan.

        > [!NOTE]
        > Tämän asetuksen seurauksena kullekin aallon etikettitaulun tietueelle tulostetaan erillinen ZPL-etiketti.

1. Sulje sivu.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Lisää kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Työtyyppi*
    - **Ehdot:** *Keräily*

    Tämä kysely varmistaa, että etikettiin tulostetaan vain keräilytyyppiset työrivit, eikä siis poispanotyyppisiä työrivejä.

1. Jos haluat tulostaa rahtikirjan tunnuksen valitse **Liitokset**-välilehdessä **Työrivit**-taulu ja liitä **Lähetykset**-taulu siihen.
1. Sulkee kyselyeditorin valintaikkuna.
1. **Tulostimen tekstiasettelu** -pikavälilehdessä on kolme osaa, johon voi kirjoittaa tulostinkoodin: **ylätunnisteosio**, **tekstiosio** ja **alatunnisteosio**. Anna **ylätunnisteosion** **Etiketin ylätunniste** -kenttään vaadittavan ylätunnisteen koodi. Jos käytössä on esimerkiksi Zebra-tulostimet voit käyttää seuraavaa koodia.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Anna **tekstiosion** **Etiketin teksti** -kenttään vaadittavan tekstin ZPL-koodi. Esimerkki:

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Anna **tekstiosion** **Etiketin alatunniste** -kenttään vaadittavan alatunnisteen ZPL-koodi. Esimerkki:

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Tämä asetus tulostaa yhden kopion kustakin etiketistä. Jos kopioita tarvitaan enemmän (esimerkiksi yksi kuormalavan kummallekin puolelle), määritä alatunnisteen **\^PQn**-osan **n**-arvoksi tarvittava määrä kopioita. Jos kutakin etikettiä halutaan tulostaa neljä kappaletta, käytä määritystä **\^PQ4**.

Etiketti on nyt käyttövalmis.

### <a name="create-a-wave-label-type"></a>Aallon etikettityypin luominen

Aallon etikettityyppien avulla aallon etikettimallit linkitetään yksikön sarjaryhmärivien yksikköön.

1. Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettityypit**.
1. Lisää aallon etikettityyppi, jossa on seuraavat asetukset:

    - **Etikettityyppi:** *Pakkaus*
    - **Kuvaus:** *Pakkaus*

### <a name="set-up-unit-sequence-groups"></a>Määritä yksikön sarjaryhmät

Seuraavaksi määritetään aallon etikettityypin yksikön sarjaryhmä.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Yksikön sarjaryhmät**.
1. Valitse **Kpl laatikko KL** -ryhmä.
1. Määritä **Laatikko**-rivin **Aallon tasotyyppi** -kentän arvoksi *Pakkaus*.

### <a name="create-a-wave-label-template"></a>Aallon etikettimallin luominen

Seuraavaksi luodaan aallon etikettityypin aallon etikettimalli.

1. Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettimallit**.
1. Lisää aallon tasomalli ja määritä seuraavat arvot ylätunnisteessa:

    - **Etikettimallin nimi:** *Pakkausetiketit*
    - **Kuvaus:** *Pakkausetiketit*
    - **Aallon vaihekoodi:** *PrintLabel*
    - **Varasto**: *62*

1. Määritä **Yleiset**-pikavälilehden **Aallon etikettityyppi** -kentän arvoksi *Pakkaus*.
1. Lisää **Aallon etikettimallin tiedot** -pikavälilehdessä uusi rivi, jolla on seuraavat asetukset:

    - **Etiketin asettelutunnus:** *Pakkaus*
    - **Tulostimen nimi:** valitse sopiva ZPL-tulostin.
    - **Suorita kysely:** *Kyllä* (Tämä asetus on valinnainen, mutta sen käyttöä suositellaan suorituskyvyn optimoinnin vuoksi.)

1. Valitse toimintoruudussa **Tallenna**.
1. Valinnainen: Jos asiakaskohtainen etikettirakenne määritetään, asiakastilin etsimistä varten on luotava kysely. Valitse **Aallon etikettimallin tiedot** -pikavälilehdessä **Muokkaa kyselyä**. Lisää sitten kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulukko:** *Lähetykset*
    - **Johdettu taulu:** *Lähetykset*
    - **Kenttä:** *Tilin numero*
    - **Ehdot:** anna soveltuvan asiakastilin numero.

    Kun olet valmis, sulje kyselyeditorin valintaikkuna valitsemalla **OK**.

1. Avaa koko etikettimallin kyselyeditorin valintaikkuna valitsemalla toimintoruudussa **Muokkaa kyselyä**.
1. Lisää kyselyeditorin valintaikkunan **Lajittelu**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Viittauksen kuormarivin tunnus (tietuetunnus)*
    - **Hakusuunta:** *Laskeva*

1. Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.
1. Avautuva sanomaruutu pyytää vahvistamaan ryhmittelyn nollaustoiminnon. Jatka valitsemalla **Kyllä**.
1. Valitse Toimintoruudussa **Aallon etiketin malliryhmä**.
1. Valitse **Aallon etiketin malliryhmä** -valintaikkunassa rivi, jossa **Viitekentän nimi** -kentän asetuksena *Viittauksen kuormarivin tunnus* ja valitse sitten rivin **Etiketin luontitunnus** -valintaruutu.

    > [!NOTE]
    > Tämä asetus luo kullekin kuormariville yhden etikettisarjan (Pakkaus 1/X) koko aallon osalta työn ryhmittelyasetuksesta riippumatta. Tämä etikettisarja voidaan tulostaa etikettiasetteluun.

### <a name="configure-number-sequence-extensions"></a>Numerosarjalaajennusten määrittäminen

Numerosarjalaajennuksilla hallitaan tiettyjen numerosarjojen GS1-vaatimustenmukaisuutta. Tämä määritys on valinnainen nykyisessä skenaariossa. Lisätietoja ja määritysohjeet ovat kohdassa [Numerosarjalaajennusten määrittäminen](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Myyntitilauksen luominen ja sen vapauttaminen varastoon

1. Valitse **Myynti ja markkinointi \> Myyntitilaus \> Kaikki myyntitilaukset**.
1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Varasto**: *62*

1. Lisää kaksi myyntitilausriviä, joilla on seuraavat asetukset:

    - Myyntitilausrivi 1:

        - **Nimiketunnus:** *A0001*
        - **Määrä** *9024*
        - **Yksikkö:** *kpl* (9024 kpl = 376 laatikkoa = 47 kuormalavaa)

    - Myyntitilausrivi 2:

        - **Nimiketunnus:** *A0002*
        - **Määrä** *9016*
        - **Yksikkö:** *kpl* (9016 kpl = 322 laatikkoa = 46 kuormalavaa)

    > [!NOTE]
    > Nämä nimikkeet ja määrät ovat vain esimerkkejä. Niiden on käytettävä aiemmin määritettyä yksikön sarjaryhmää, niille on määritettävä soveltuva yksikkömuunnos *kappaleesta* *laatikkoon* ja edelleen *kuormalavaksi* ja niiden varaston on oltava varastossa *62*. Lisätietoja on kohdassa [Mittayksikkö ja varastointikäytännöt](unit-measure-stocking-policies.md).

1. Valitse tilausrivi 1. Valitse sitten **Myyntitilausrivi**-osan **Varasto**-valikossa **Varaukset**.
1. Valitse **Varaus**-sivun toimintoruudussa **Varaa erä** ja sulje sitten sivu.
1. Toista vaiheet 4 ja 5 myyntitilausriville 2.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

    Seuraavat tapahtumat:

    - Järjestelmä käsittelee luodun lähetyksen käyttämällä etiketin tulostusvaiheen sisältävää mallia. Etiketin asettelun avulla määritetään etiketin muoto, ja näin saatu etiketti tulostetaan etikettimallissa valitulla tulostimella.
    - Aallon etiketit luodaan ja tulostetaan. Etikettien ja pakkausten määrä on sama (tässä esimerkiksi rivillä 1 on 376 laatikkoetikettiä ja rivillä 2 niitä on 322).
    - Lähetyksille luodaan uusi rahtikirjan tunnus. Jos numerosarjalaajennukset määritettiin, aallon etikettitunnus noudattaa **SSCC-18**-lukumuotoilua. 

Voit tarkastella aallon etikettejä ja tulostaa niitä uudelleen seuraavilta sivuilta. Valitse kunkin sivun toimintoruudun **Lähetykset**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Aallon etiketit**.

- Kaikki lähetykset \> Lähetyksen tiedot
- Kaikki kuormat \> Kuorman tiedot
- Kaikki aallot
- Aalto-otsikot
- Aallon etikettihistoria

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>Skenaario 2: Aallon konttiinpakkauksen etikettitulostus (ilman aallon etikettitietueita)

Tässä skenaariossa tulostetaan aallon etikettejä konttipakkausta käytettäessä. Tällä tavoin nimikkeet jaetaan automaattisesti pakkauksiin eikä aallon etikettitietuetta tarvita. Tässä tapauksessa kontin tunnus toimii SSCC-koodin paikkamerkkinä.

Tämä skenaarion ja skenaarion 1 tärkeimmät erot:

- **Aallon etikettimallit:** Aallon etikettityyppiä ei valita aallon etikettimallissa eikä etiketin luontiryhmittelyä tarvita. Muutoin aallon etikettimalli määritetään ja linkitys aaltomalliin tehdään skenaariossa 1 kuvatulla tavalla. Aallon etikettityyppi on jätettävä tyhjäksi, sillä se estää aallon etikettien luonnin.
- **Aallon etiketin asettelut:** Aallon etikettiasettelun riviasettelut tehdään työriveillä eikä aallon etikettitietueille. Etikettiasettelun riviasetus on määritettävä käyttämällä **WHSWorkLine**-taulua eikä **WHSWaveLabel**-taulua. **Riviä sivua kohden** -asetus määrittää, kuinka monta riviä tekstiosassa on. 

Tämä määritys sopii myös liiketoimintaskenaarioihin, joissa useita eri nimikkeitä pakataan yhteen etiketilliseen laatikkoon tai kuormalavalle, ja tämä pakkausprosessi voidaan määrittää työn luonnilla (kuten lähetyksen mukaan ryhmitetty työ).

Tämä skenaario sisältää työnkulun alusta loppuun.

### <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Tämän skenaarion käyttäminen edellyttää, että demotiedot on asennettu ja että **USMF**-yritys on valittu.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Aallon etikettimenetelmän saatavuuden varmistaminen

On mahdollista, että aallon käsittelymenetelmät on luotava uudelleen, jotta aallon etiketin tulostusmenetelmä on käytettävissä.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.
1. Varmista, että **waveLabelPrinting** on luettelossa. Jos se ei ole luettelossa, lisää se valitsemalla toimintoruudussa **Luo menetelmät uudelleen**.

### <a name="set-up-a-wave-template"></a>Aaltomallin asetuksien määrittäminen

Aaltomallin avulla tietyt aaltomenetelmien esiintymät voidaan linkittää vastaavaan aallon etikettimalliin.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Valitse malli, kuten **63 Konttiinpakkaus**.
1. Siirrä **Aallon etiketin tulostus** -menetelmä **Menetelmät**-pikavälilehdessä **Valitut menetelmät** -sarakkeeseen.
1. Valitse **Valitut menetelmät** -sarakkeessa **Aallon etiketin tulostus** -menetelmä ja valitsen sen **Aallon vaihekoodi** -kentässä *PrintLabel*. Lisätietoja aallon vaihekoodeista on kohdassa [Aallon vaihekoodit](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Aallon etikettiasettelun luominen

1. Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etiketin asettelut**.
1. Luo tietue, jossa on seuraavat asetukset:

    - **Etiketin asettelutunnus:** *Pakkaus*
    - **Kuvaus:** *Pakkaus (SSCC)*

1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Aallon etiketin riviasetukset**.

    **Aallon etiketin riviasetukset** -sivu avautuu. Etiketin dynaaminen osa määritetään tällä sivulla.

1. Lisää rivi, jossa on seuraavat asetukset:

    - **Rivin tunnus:** *WorkLine*
    - **Rivin taulukon nimi:** *WHSWorkLine*
    - **Rivin lähtökohta:** *500*

        Tämä kenttä määrittää pystysuunnassa paikan, josta rivi alkaa etiketissä.

    - **Rivin korkeus:** *-50*

        Tämä kenttä määrittää kunkin rivin korkeuden. Rivin korkeus on positiivinen vaakasuuntaisissa etiketeissä ja negatiivinen pystysuuntaisissa etiketeissä.

    - **Riviä sivua kohden:** *5*

        Tämä kenttä määrittää, kuinka monta riviä kuhunkin etikettiin tulostetaan.

        > [!NOTE]
        > Tämä asetus tulostaa kullekin työlle useita ZPL-etikettejä, ja kullakin sivulla voi olla enintään viisi työriviä. Jos esimerkiksi konttiin tulostettavassa etiketissä on 12 riviä, etikettejä tulostetaan kolme. Jos haluat tulostaa erillisen etiketin kullekin keräilyriville, määritä arvoksi *1*.

1. Sulje sivu.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Lisää kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Työtyyppi*
    - **Ehdot:** *Keräily*

1. Jos haluat tulostaa rahtikirjan tunnuksen valitse **Liitokset**-välilehdessä **Työrivit**-taulu ja liitä **Lähetykset**-taulu siihen.
1. Sulkee kyselyeditorin valintaikkuna.
1. **Tulostimen tekstiasettelu** -pikavälilehdessä on kolme osaa, johon voi kirjoittaa tulostinkoodin: **ylätunnisteosio**, **tekstiosio** ja **alatunnisteosio**. Anna **ylätunnisteosion** **Etiketin ylätunniste** -kenttään vaadittavan ylätunnisteen koodi. Jos käytössä on esimerkiksi Zebra-tulostimet voit käyttää seuraavaa koodia.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Anna **tekstiosion** **Etiketin teksti** -kenttään vaadittavan tekstin ZPL-koodi. Esimerkki:

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. Anna **tekstiosion** **Etiketin alatunniste** -kenttään vaadittavan alatunnisteen ZPL-koodi. Esimerkki:

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Tämä asetus tulostaa yhden kopion kustakin etiketistä. Jos kopioita tarvitaan enemmän (esimerkiksi yksi kuormalavan kummallekin puolelle), määritä alatunnisteen **\^PQn**-osan **n**-arvoksi tarvittava määrä kopioita. Jos kutakin etikettiä halutaan tulostaa neljä kappaletta, käytä määritystä **\^PQ4**.

Etiketti on nyt käyttövalmis.

### <a name="create-a-wave-label-template"></a>Aallon etikettimallin luominen

1. Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettimallit**.
1. Lisää aallon tasomalli ja määritä seuraavat arvot ylätunnisteessa:

    - **Etikettimallin nimi:** *Konttietiketit*
    - **Kuvaus:** *Konttietiketit*
    - **Aallon vaihekoodi:** *PrintLabel*
    - **Varasto**: *63*

1. Lisää **Aallon etikettimallin tiedot** -pikavälilehdessä rivi, jolla on seuraavat asetukset:

    - **Etiketin asettelutunnus:** *Kontti*
    - **Tulostimen nimi:** valitse sopiva ZPL-tulostin.
    - **Suorita kysely:** *Kyllä* (Tämä asetus on valinnainen, mutta sen käyttöä suositellaan suorituskyvyn optimoinnin vuoksi.)

1. Valitse toimintoruudussa **Tallenna**.
1. Valinnainen: Jos asiakaskohtainen etikettirakenne määritetään, asiakastilin etsimistä varten on luotava kysely. Valitse **Aallon etikettimallin tiedot** -pikavälilehdessä **Muokkaa kyselyä**. Lisää sitten kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulukko:** *Lähetykset*
    - **Johdettu taulu:** *Lähetykset*
    - **Kenttä:** *Tilin numero*
    - **Ehdot:** anna soveltuvan asiakastilin numero.

    Kun olet valmis, sulje kyselyeditorin valintaikkuna valitsemalla **OK**.

### <a name="configure-number-sequence-extensions"></a>Numerosarjalaajennusten määrittäminen

Numerosarjalaajennuksilla hallitaan tiettyjen numerosarjojen GS1-vaatimustenmukaisuutta. Tämä määritys on valinnainen nykyisessä skenaariossa. Lisätietoja ja määritysohjeet ovat kohdassa [Numerosarjalaajennusten määrittäminen](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Myyntitilauksen luominen ja sen vapauttaminen varastoon

1. Valitse **Myynti ja markkinointi \> Myyntitilaus \> Kaikki myyntitilaukset**.
1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Varasto**: *63*

1. Lisää viisi myyntitilausriviä:

    - Myyntitilausrivi 1:

        - **Nimiketunnus:** *A0001*
        - **Määrä** *10*

    - Myyntitilausrivi 2:

        - **Nimiketunnus:** *A0002*
        - **Määrä** *20*

    - Myyntitilausrivi 3:

        - **Nimiketunnus:** *L0006*
        - **Määrä** *20*

    - Myyntitilausrivi 4:

        - **Nimiketunnus:** *L0100*
        - **Määrä** *40*

    - Myyntitilausrivi 5:

        - **Nimiketunnus:** *L0101*
        - **Määrä** *50*

    > [!NOTE]
    > Nämä nimikkeet ja määrät ovat vain esimerkkejä. Niiden on oltava varastossa määritetyssä varastossa.

1. Valitse tilausrivi 1. Valitse sitten **Myyntitilausrivi**-osan **Varasto**-valikossa **Varaukset**.
1. Valitse **Varaus**-sivun toimintoruudussa **Varaa erä** ja sulje sitten sivu.
1. Toista vaiheet 4 ja 5 kullekin lisätylle myyntitilausriville.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

    Seuraavat tapahtumat:

    - Järjestelmä käsittelee luodun lähetyksen käyttämällä etiketin tulostusvaiheen sisältävää mallia. Etiketin asettelun avulla määritetään etiketin muoto, ja näin saadussa etiketissä on viisi riviä ja se tulostetaan etikettimallissa valitulla tulostimella.
    - Lähetyksille luodaan uusi rahtikirjan tunnus. Jos numerosarjalaajennukset määritettiin, aallon etikettitunnus noudattaa **SSCC-18**-lukumuotoilua. 

Voit tulostaa nämä aallon etiketit uudelleen valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Aallon etiketin historia**.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>Skenaario 3: Moneen tasoon luokiteltujen etikettien aallon etikettitulostus

Tässä skenaariossa näytetään, miten aallon etiketin tulostustoimintoa käytetään, kun varastoprosessit edellyttävät moneen tasoon luokiteltuja lähetyksen etikettejä. Esimerkiksi pakkauksille ja kuormalavoille on voitava tulostaa eri etiketit, ja koko lähetykselle on voitava tulostaa keskeytysetiketti. Keskeytysetiketit ovat erillinen etikettityyppi, joita voidaan käyttää rullien ja konttien välissä, kuten lähetystunnuksen etikettien ja viivakoodin välillä. Tällä tavoin etiketit on helppo lajitella tulostuksen jälkeen.

Suurin ero tämän skenaarion ja skenaarion 1 määrityksissä on keskeytysetikettien käyttöönoton lisäksi se, että useita etikettityyppejä on liitettävä aallon etikettimalleihin ja yksikön sarjaryhmäriveihin. Tämä määritys tehdään määrittämällä seuraavat elementit tässä skenaariossa:

- **Aallon käsittelymenetelmät:** aallon etikettimenetelmän merkitään toistettavaksi, se lisätään vähintään kaksi kertaa aaltomalliin ja erilaiset aallon vaihekoodit määritetään.
- **Aallon etikettimallit:** Aallon etikettimallit määritetään ja ne linkitetään aaltomalliin. Kullakin aallon etikettimallilla on oltava oma aallon etikettityyppi.
- **Aallon etiketin asettelut:** Useita aallon etiketin asetteluja luodaan. Jokaisella etiketin tasolla on erillinen etiketin asettelu, minkä lisäksi keskeytysetiketillä on oma asettelu.

Tämä skenaario sisältää työnkulun alusta loppuun.

### <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Tämän skenaarion käyttäminen edellyttää, että demotiedot on asennettu ja että **USMF**-yritys on valittu.

### <a name="set-up-a-wave-process-method"></a>Aallon käsittelymenetelmän määrittäminen

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.
1. Varmista, että **waveLabelPrinting** on luettelossa. Jos se ei ole luettelossa, lisää se valitsemalla toimintoruudussa **Luo menetelmät uudelleen**.
1. Valitse **waveLabelPrinting**-menetelmässä **Tee menetelmästä toistettava** -valintaruutu.

### <a name="set-up-a-wave-template"></a>Aaltomallin asetuksien määrittäminen

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
2. Valitse malli, kuten **62 Lähetyksen oletus**.
3. Siirrä **Aallon etiketin tulostus** -menetelmä **Menetelmät**-pikavälilehdessä **Valitut menetelmät** -sarakkeeseen.
4. Määritä **Valitut menetelmät** -sarakkeessa **Aallon vaihekoodi** -arvo, kuten *Pakkaus*, **Aallon etiketin tulostus** -menetelmään. Lisätietoja aallon vaihekoodeista on kohdassa [Aallon vaihekoodit](wave-step-codes.md).
5. Siirrä **Aallon etiketin tulostus** -menetelmä **Valitut menetelmät** -sarakkeeseen toisen kerran.
6. Määritä **Valitut menetelmät** -sarakkeessa toinen **Aallon vaihekoodi** -arvo, kuten *Kuormalava*, toiseen **Aallon etiketin tulostus** -menetelmään. Lisätietoja aallon vaihekoodeista on kohdassa [Aallon vaihekoodit](wave-step-codes.md).

### <a name="create-three-wave-label-layouts"></a>Kolmen aallon etikettiasettelun luominen

1. Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etiketin asettelut**.
1. Luo tietue, jossa on seuraavat asetukset:

    - **Etiketin asettelutunnus:** *Pakkaus*
    - **Kuvaus:** *Pakkaus (SSCC)*

1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Aallon etiketin riviasetukset**.

    **Aallon etiketin riviasetukset** -sivu avautuu. Etiketin dynaaminen osa määritetään tällä sivulla.

1. Lisää rivi, jossa on seuraavat asetukset:

    - **Rivin tunnus:** *WaveLabel*
    - **Rivin taulukon nimi:** *WHSWaveLabel*
    - **Rivin lähtökohta:** *0*

        Tämä kenttä määrittää pystysuunnassa paikan, josta rivi alkaa etiketissä.

    - **Rivin korkeus:** *0*

        Tämä kenttää määrittää kunkin rivin korkeuden (pisteinä) ZPL-standardin mukaisesti. Rivin korkeus on positiivinen vaakasuuntaisissa etiketeissä ja negatiivinen pystysuuntaisissa etiketeissä. Koska tässä esimerkissä on vain yksi rivi, arvoksi voidaan määrittää *0* (nolla).

    - **Riviä sivua kohden:** *1*

        Tämä kenttä määrittää, kuinka monta riviä kuhunkin etikettiin tulostetaan.

        > [!NOTE]
        > Tämän asetuksen seurauksena kullekin aallon etikettitaulun tietueelle tulostetaan erillinen ZPL-etiketti.

1. Sulje sivu.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Lisää kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Työtyyppi*
    - **Ehdot:** *Keräily*

    Tämä kysely varmistaa, että etikettiin tulostetaan vain keräilytyyppiset työrivit, eikä siis poispanotyyppisiä työrivejä.

1. Jos haluat tulostaa rahtikirjan tunnuksen valitse **Liitokset**-välilehdessä **Työrivit**-taulu ja liitä **Lähetykset**-taulu siihen. 
1. Sulkee kyselyeditorin valintaikkuna.
1. **Tulostimen tekstiasettelu** -pikavälilehdessä on kolme osaa, johon voi kirjoittaa tulostinkoodin: **ylätunnisteosio**, **tekstiosio** ja **alatunnisteosio**. Anna **ylätunnisteosion** **Etiketin ylätunniste** -kenttään vaadittavan ylätunnisteen koodi. Jos käytössä on esimerkiksi Zebra-tulostimet voit käyttää seuraavaa koodia.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Anna **tekstiosion** **Etiketin teksti** -kenttään vaadittavan tekstin ZPL-koodi. Esimerkki:

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Anna **tekstiosion** **Etiketin alatunniste** -kenttään vaadittavan alatunnisteen ZPL-koodi. Esimerkki:

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Tämä asetus tulostaa yhden kopion kustakin etiketistä. Jos kopioita tarvitaan enemmän (esimerkiksi yksi kuormalavan kummallekin puolelle), määritä alatunnisteen **\^PQn**-osan **n**-arvoksi tarvittava määrä kopioita. Jos kutakin etikettiä halutaan tulostaa neljä kappaletta, käytä määritystä **\^PQ4**.

1. Ensimmäinen etiketti on nyt käyttövalmis.
1. Luo toinen asettelutietue, jossa on seuraavat asetukset:

    - **Etiketin asettelutunnus:** *Kuormalava*
    - **Kuvaus:** *Kuormalava*

1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Aallon etiketin riviasetukset**.

    **Aallon etiketin riviasetukset** -sivu avautuu. Etiketin dynaaminen osa määritetään tällä sivulla.

1. Lisää rivi, jossa on seuraavat asetukset:

    - **Rivin tunnus:** *WaveLabel*
    - **Rivin taulukon nimi:** *WHSWaveLabel*
    - **Rivin lähtökohta:** *0*

        Tämä kenttä määrittää pystysuunnassa paikan, josta rivi alkaa etiketissä.

    - **Rivin korkeus:** *0*

        Tämä kenttää määrittää kunkin rivin korkeuden (pisteinä) ZPL-standardin mukaisesti. Rivin korkeus on positiivinen vaakasuuntaisissa etiketeissä ja negatiivinen pystysuuntaisissa etiketeissä. Koska tässä esimerkissä on vain yksi rivi, arvoksi voidaan määrittää *0* (nolla).

    - **Riviä sivua kohden:** *1*

        Tämä kenttä määrittää, kuinka monta riviä kuhunkin etikettiin tulostetaan.

        > [!NOTE]
        > Tällä asetuksella kullekin aallon etikettitaulun tietueelle tulostetaan erillinen ZPL-etiketti.

1. Sulje sivu.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Lisää kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Työtyyppi*
    - **Ehdot:** *Keräily*

    Tämä kysely varmistaa, että etikettiin tulostetaan vain keräilytyyppiset työrivit, eikä siis poispanotyyppisiä työrivejä.

1. Jos haluat tulostaa rahtikirjan tunnuksen valitse **Liitokset**-välilehdessä **Työrivit**-taulu ja liitä **Lähetykset**-taulu siihen.
1. Sulkee kyselyeditorin valintaikkuna.
1. **Tulostimen tekstiasettelu** -pikavälilehdessä on kolme osaa, johon voi kirjoittaa tulostinkoodin: **ylätunnisteosio**, **tekstiosio** ja **alatunnisteosio**. Anna **ylätunnisteosion** **Etiketin ylätunniste** -kenttään vaadittavan ylätunnisteen koodi. Jos käytössä on esimerkiksi Zebra-tulostimet voit käyttää seuraavaa koodia.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Anna **tekstiosion** **Etiketin teksti** -kenttään vaadittavan tekstin ZPL-koodi. Esimerkki:

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. Anna **tekstiosion** **Etiketin alatunniste** -kenttään vaadittavan alatunnisteen ZPL-koodi. Esimerkki:

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Tämä asetus tulostaa yhden kopion kustakin etiketistä. Jos kopioita tarvitaan enemmän (esimerkiksi yksi kuormalavan kummallekin puolelle), määritä alatunnisteen **\^PQn**-osan **n**-arvoksi tarvittava määrä kopioita. Jos kutakin etikettiä halutaan tulostaa neljä kappaletta, käytä määritystä **\^PQ4**.

1. Toinen etiketti on nyt käyttövalmis.
1. Luo kolmas asettelutietue, jossa on seuraavat asetukset:

    - **Etiketin asettelutunnus:** *Keskeytys*
    - **Kuvaus:** *Keskeytysetiketti*

1. Valitse toimintoruudussa **Tallenna**.
1. **Tulostimen tekstiasettelu** -pikavälilehdessä on kolme osaa, johon voi kirjoittaa tulostinkoodin: **ylätunnisteosio**, **tekstiosio** ja **alatunnisteosio**. Anna **ylätunnisteosion** **Etiketin ylätunniste** -kenttään vaadittavan ylätunnisteen ZPL-koodi. Esimerkki:

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Tällä kertaa tekstiosaa ei tarvita. Anna tämän vuoksi tarvittava teksti **alatunnisteosiossa**. Esimerkki:

    ```plaintext
    ^XZ
    ```

    Kolmas etiketti on nyt käyttövalmis.

    > [!NOTE]
    > Tämä kolmas etiketti on keskeytysetiketti, joka erottaa etikettirullat toisistaan.

### <a name="create-two-wave-label-types"></a>Kahden aallon etikettityypin luominen

1. Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettityypit**.
1. Luo tietue, jossa on seuraavat asetukset:

    - **Etikettityyppi:** *Pakkaus*
    - **Kuvaus:** *Pakkaus*

1. Luo toinen tietue, jossa on seuraavat asetukset:

    - **Etikettityyppi:** *Kuormalava*
    - **Kuvaus:** *Kuormalava*

### <a name="set-up-unit-sequence-groups"></a>Määritä yksikön sarjaryhmät

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Yksikön sarjaryhmät**.
1. Valitse tai luo **Kpl laatikko KL** -ryhmä.
1. Määritä **Laatikko**-rivin **Aallon tasotyyppi** -kentän arvoksi *Pakkaus*.
1. Määritä **Kuormalava**-rivin **Aallon tasotyyppi** -kentän arvoksi *Kuormalava*.

### <a name="create-wave-label-templates"></a>Aallon etikettimallien luominen

1. Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettimallit**.
1. Luo etikettimalli, jossa on seuraavat asetukset:

    - **Etikettimallin nimi:** *Pakkausetiketit*
    - **Kuvaus:** *Pakkausetiketit*
    - **Aallon vaihekoodi:** *Pakkaus*
    - **Varasto**: *62*

1. Valitse **Yleinen**-pikavälilehden **Aallon etikettityyppi**-kentässä arvo, kuten *Pakkaus*.
1. Lisää **Aallon etikettimallin tiedot** -pikavälilehdessä rivi, jolla on seuraavat asetukset:

    - **Etiketin asettelutunnus:** *Pakkaus*
    - **Tulostimen nimi:** valitse sopiva ZPL-tulostin.
    - **Suorita kysely:** *Kyllä* (Tämä asetus on valinnainen, mutta sen käyttöä suositellaan suorituskyvyn optimoinnin vuoksi.)

1. Valitse toimintoruudussa **Tallenna**.
1. Valinnainen: Jos asiakaskohtainen etikettirakenne määritetään, asiakastilin etsimistä varten on luotava kysely. Valitse **Aallon etikettimallin tiedot** -pikavälilehdessä **Muokkaa kyselyä**. Lisää sitten kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulukko:** *Lähetykset*
    - **Johdettu taulu:** *Lähetykset*
    - **Kenttä:** *Tilin numero*
    - **Ehdot:** anna soveltuvan asiakastilin numero.

    Kun olet valmis, sulje kyselyeditorin valintaikkuna valitsemalla **OK**.

1. Avaa koko etikettimallin kyselyeditorin valintaikkuna valitsemalla toimintoruudussa **Muokkaa kyselyä**.
1. Lisää kyselyeditorin valintaikkunan **Lajittelu**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Viittauksen kuormarivin tunnus (tietuetunnus)*
    - **Hakusuunta:** *Laskeva*

1. Lisää toinen rivi, jossa on seuraavat asetukset:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Lähetyksen tunnus*
    - **Hakusuunta:** *Laskeva*

1. Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.
1. Avautuva sanomaruutu pyytää vahvistamaan ryhmittelyn nollaustoiminnon. Jatka valitsemalla **Kyllä**.
1. Valitse Toimintoruudussa **Aallon etiketin malliryhmä**.
1. Määritä **Aalloin etiketin malliryhmä** -valintaikkunassa seuraavat arvot sille riville, jonka **Viitekentän nimi** -kentän asetuksena on *Lähetyksen tunnus*:

    - **Tulosta keskeytysetiketti:** valitse tämä valintaruutu.
    - **Etiketin asettelutunnus:** Valitse keskeytysetiketti. (Valitse esimerkiksi aiemmin tässä skenaariossa luotu *Keskeytys*-etiketti.)
    - **Tulostiminen nimi:** Valitse keskeytysetiketin tulostin. (Yleensä etikettirullien jakamista varten on syytä valita sama tulostin, joka valittiin **Aallon etikettimallin tiedot** -pikavälilehdessä. Muutkin skenaariot ovat kuitenkin mahdollisia.)

1. Valitse rivillä, jonka **Viitekentän nimi** -kentän asetuksena on *Viittauksen kuormarivin tunnus*, **Etiketin luontitunnus** -valintaruutu.

    > [!NOTE]
    > Tämä asetus luo kullekin kuormariville yhden etikettisarjan (Pakkaus 1/X) koko aallon osalta työn ryhmittelyasetuksesta riippumatta. Tämä etikettisarja voidaan tulostaa etikettiasetteluun. Lisäksi eri lähetysten etiketit erotetaan valitulla keskeytysetiketillä.

1. Sulje **Aallon etiketin malliryhmä** -valintaikkuna valitsemalla **OK**.
1. Luo toinen etikettimalli, jossa on seuraavat asetukset:

    - **Etikettimallin nimi:** *Kuormalavaetiketit*
    - **Kuvaus:** *Kuormalavaetiketit*
    - **Aallon vaihekoodi:** *Kuormalava*
    - **Varasto**: *62*

1. Valitse **Yleinen**-pikavälilehden **Aallon etikettityyppi**-kentässä arvo, kuten *Kuormalava*.
1. Lisää **Aallon etikettimallin tiedot** -pikavälilehdessä rivi, jolla on seuraavat asetukset:

    - **Etiketin asettelutunnus:** *Kuormalava*
    - **Tulostimen nimi:** valitse sopiva ZPL-tulostin.
    - **Suorita kysely:** *Kyllä* (Tämä asetus on valinnainen, mutta sen käyttöä suositellaan suorituskyvyn optimoinnin vuoksi.)

1. Valitse toimintoruudussa **Tallenna**.
1. Valinnainen: Jos asiakaskohtainen etikettirakenne määritetään, asiakastilin etsimistä varten on luotava kysely. Valitse **Aallon etikettimallin tiedot** -pikavälilehdessä **Muokkaa kyselyä**. Lisää sitten kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulukko:** *Lähetykset*
    - **Johdettu taulu:** *Lähetykset*
    - **Kenttä:** *Tilin numero*
    - **Ehdot:** anna soveltuvan asiakastilin numero.

    Kun olet valmis, sulje kyselyeditorin valintaikkuna valitsemalla **OK**. 

1. Avaa koko etikettimallin kyselyeditorin valintaikkuna valitsemalla toimintoruudussa **Muokkaa kyselyä**.
1. Lisää kyselyeditorin valintaikkunan **Lajittelu**-välilehdessä rivi, jolla on seuraavat asetukset:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Viittauksen kuormarivin tunnus (tietuetunnus)*
    - **Hakusuunta:** *Laskeva*

1. Lisää toinen rivi, jossa on seuraavat asetukset:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Lähetyksen tunnus*
    - **Hakusuunta:** *Laskeva*

1. Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.
1. Avautuva sanomaruutu pyytää vahvistamaan ryhmittelyn nollaustoiminnon. Jatka valitsemalla **Kyllä**.
1. Valitse Toimintoruudussa **Aallon etiketin malliryhmä**.
1. Määritä **Aalloin etiketin malliryhmä** -valintaikkunassa seuraavat arvot sille riville, jonka **Viitekentän nimi** -kentän asetuksena on *Lähetyksen tunnus*:

    - **Tulosta keskeytysetiketti:** valitse tämä valintaruutu.
    - **Etiketin asettelutunnus:** Valitse keskeytysetiketti. (Valitse esimerkiksi aiemmin tässä skenaariossa luotu *Keskeytys*-etiketti.)
    - **Tulostiminen nimi:** Valitse keskeytysetiketin tulostin. (Yleensä etikettirullien jakamista varten on syytä valita sama tulostin, joka valittiin **Aallon etikettimallin tiedot** -pikavälilehdessä. Muutkin skenaariot ovat kuitenkin mahdollisia.)

1. Valitse rivillä, jonka **Viitekentän nimi** -kentän asetuksena on *Viittauksen kuormarivin tunnus*, **Etiketin luontitunnus** -valintaruutu.

    > [!NOTE]
    > Tämä asetus luo kullekin kuormariville yhden etikettisarjan (Pakkaus 1/X) koko aallon osalta työn ryhmittelyasetuksesta riippumatta. Tämä etikettisarja voidaan tulostaa etikettiasetteluun. Lisäksi eri lähetysten etiketit erotetaan valitulla keskeytysetiketillä.

### <a name="configure-number-sequence-extensions"></a>Numerosarjalaajennusten määrittäminen

Numerosarjalaajennuksilla hallitaan tiettyjen numerosarjojen GS1-vaatimustenmukaisuutta. Tämä määritys on valinnainen nykyisessä skenaariossa. Lisätietoja ja määritysohjeet ovat kohdassa [Numerosarjalaajennusten määrittäminen](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Myyntitilauksen luominen ja sen vapauttaminen varastoon

1. Valitse **Myynti ja markkinointi \> Myyntitilaus \> Kaikki myyntitilaukset**.
1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Varasto**: *62*

1. Lisää kaksi myyntitilausriviä:

    - Myyntitilausrivi 1:

        - **Nimiketunnus:** *A0001*
        - **Määrä** *9024*
        - **Yksikkö:** *kpl* (9024 kpl = 376 laatikkoa = 47 kuormalavaa)

    - Myyntitilausrivi 2:

        - **Nimiketunnus:** *A0002*
        - **Määrä** *9016*
        - **Yksikkö:** *kpl* (9016 kpl = 322 laatikkoa = 46 kuormalavaa)

    > [!NOTE]
    > Nämä nimikkeet ja määrät ovat vain esimerkkejä. Niiden on käytettävä aiemmin määritettyä yksikön sarjaryhmää, niille on määritettävä soveltuva yksikkömuunnos *kappaleesta* *laatikkoon* ja edelleen *kuormalavaksi* ja niiden varaston on oltava varastossa *62*. Lisätietoja on kohdassa [Mittayksikkö ja varastointikäytännöt](unit-measure-stocking-policies.md).

1. Valitse tilausrivi 1. Valitse sitten **Myyntitilausrivi**-osan **Varasto**-valikossa **Varaukset**.
1. Valitse **Varaus**-sivun toimintoruudussa **Varaa erä** ja sulje sitten sivu.
1. Toista vaiheet 4 ja 5 myyntitilausriville 2.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

    Seuraavat tapahtumat: 

    - Järjestelmä käsittelee luodun lähetyksen käyttämällä etiketin tulostusvaiheen sisältävää mallia. Etiketin asettelun avulla määritetään etiketin muoto, ja näin saatu etiketti tulostetaan etikettimallissa valitulla tulostimella.
    - Aallon etiketit luodaan ja tulostetaan. Etikettien määrä on sama kuin pakkausten määrä. (Tässä esimerkissä rivillä 1 on 376 laatikkoetikettiä ja rivillä 2 on 322 laatikkoetikettiä; rivillä 1 on 47 kuormalavaetikettiä ja rivillä 2 on 47 kuormalavaetikettiä, minkä lisäksi kahdessa keskeytysetiketissä on lähetyksen tunnus.)
    - Lähetyksille luodaan uusi rahtikirjan tunnus. Jos numerosarjalaajennukset määritettiin, aallon etikettitunnus noudattaa **SSCC-18**-lukumuotoilua. 

Voit tarkastella aallon etikettejä ja tulostaa niitä uudelleen seuraavilta sivuilta:

- Kaikki lähetykset \> Lähetyksen tiedot
- Kaikki kuormat \> Kuorman tiedot
- Kaikki aallot
- Aalto-otsikot
- Aallon etikettihistoria

Useimmilla näistä sivuista sopiva toiminto löytyy valitsemalla **Aallon etiketit** toimintoruudun **Lähetykset**-välilehden **Liittyvät tiedot** -ryhmässä.

## <a name="additional-resources"></a>Lisäresurssit

- [Aallon etikettien tulostaminen uudelleen ja mitätöinti](reprint-and-void-wave-labels.md)
- [Aallon etikettien tulostamisen ajoittaminen aallon aikana](configure-task-based-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
