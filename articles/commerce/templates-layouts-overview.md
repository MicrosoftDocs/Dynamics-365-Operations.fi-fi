---
title: Mallit ja asettelut – yleiskatsaus
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commercen malleja ja asetteluja.
author: phinneyridge
ms.date: 12/12/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: e0bf7e942339775b2e9ee15060d555be07c1cdc5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277930"
---
# <a name="templates-and-layouts-overview"></a>Mallit ja asettelut – yleiskatsaus


[!include [banner](includes/banner.md)]

Mallit ovat Microsoft Dynamics 365 Commerce -sivumallin peruselementtejä. Jos tavoitteenasi on maksimoida sivuston muokkaustyönkulkujen tehokkuus ja yhdenmukaisuus, on tärkeää, että opit hyödyntämään sivustosi malleja. Mallirakennetta koskevat varhaiset päätökset ovat tärkeitä. Ne voivat vaikuttaa merkittävästi päivittäisiin ja kausittaisiin päivityksiin sekä koko sivustoa koskeviin tuotemerkkipäivityksiin. Hyvin muotoillut mallit auttavat myös muilla tavoin. Ne auttavat esimerkiksi kaikkien sivustojen hakukoneoptimoinnin pisteiden parantamisessa ja virhemäärän minimoimisessa.

Mallien käsitteleminen kannattaa aloittaa siitä, että ymmärtää mallien ja asettelujen toiminnalliset hyödyt, niiden erot ja hierarkian.

Seuraavassa kuvassa on sivun mallihierarkia muodostetulla verkkosivulla.

![Sivu mallikaavio.](../commerce/media/page-model-diagram.png)

| Entiteetti        | Perustoiminto |
|---------------|----------------|
| Sapluuna      | Mallit määrittävät asettelujen ja sivuesiintymien joukon moduuliasetukset ja perusasetukset. |
| Asettelu (layout)        | Asettelut määrittävät sivun tai sivujoukon moduulien lopullisen valinnan ja järjestyksen. |
| Sivuesiintymä | Sivuesiintymät määrittävät tiettyjen sivujen tiedot ja sisällön. |

## <a name="templates"></a>Mallit

Mallit ovat Dynamics 365 Commerce -sivun mallihierarkian ylätaso. Ne edustavat sivuston määrityksen tärkeää varhaista vaihetta. Mallien avulla valvotaan alitason asettelujen ja sivujen yhdenmukaisuutta. Se tehdään määrittämällä perusrakenne ja muokkaustyökaluvalinnat verkosta tietoja lataamalla tehtävän asettelun luomisen ja sivun luomisen työnkulkuja varten. Mallit auttavat sisällön muokkausprosessin yksinkertaistamisessa ennalta määritettyjen ja keskitetysti hallittujen elementtien (esimerkiksi ylä- ja alaotsikot) sekä ohjattujen muokkaustyönkulkujen osalta. Ohjatut muokkaustyönkulut auttavat moduulin määritysvaihtoehtojen pitämisessä tuotemerkkikohtaisina.

### <a name="controlling-consistency"></a>Yhdenmukaisuuden hallinta

Kun suunnittelet mallin, tärkein liiketoimintaa koskeva päätös on se, miten paljon malli hallitsee sivun luontiprosessia. Malli, joka jättää kaiken avoimeksi verkosta tietoja lataavaa tekijää varten, on helpoiten luotava mallityyppi. Tämän mallin käyttämisellä voi kuitenkin olla pitkäaikaisia vaikutuksia sivuihin, jotka on luotu kyseisen mallin avulla. Hyvin kirjoitettu malli sisältää ohjeet ja tarjoaa tehostetun muokkauskokemuksen. Näiden lisäksi se antaa tekijöille riittävästi joustavuutta, jotta he voivat suorittaa tehtävän loppuun. Kaikki nämä seikat riippuvat mallin käyttämästä hallinnan tasosta.

Mallien avulla sisällöntekijät voivat tehostaa toimintaansa ja noudattaa tuotemerkin vaatimuksia seuraavasti:

- Rajoita sivulla käytettävien moduulien määrää.
- Ehdota oletusmoduulia ja määrityksen oletusvalintoja.
- Tee tiettyjä moduuli- ja määritysvalintoja, joita hallitaan mallin tasolla. Tätä prosessia kutsutaan myös asetuksen *lukitsemiseksi*.

Seuraavassa esimerkissä näkyy, miten perusmalli (malli X) voidaan määrittää:

- Kaikilla mallin X alitason asetteluilla on oltava ylätunnisteen, tekstiosan ja alatunnisteen säilö.
- Mallissa X ylätunnisteen säilön määritys on lukittu. Sitä voi muuttaa vain mallissa X. Kaikilla alitason asetteluilla ja sivuilla on aina tämä ylätunniste.
- Tekstiosan säilössä on oltava vähintään yksi moduuli. Siinä voi olla enintään kymmenen moduulia. Nämä moduulit määritetään verkosta ladattavilla asetteluilla ja sivuilla.
- Tekstiosan säilön hero-, ominaisuus-, karuselli- ja ilmoituspalkkimoduulit ovat käytettävissä.
- Alatunnisteen säilö määritetään mallissa X. Se voidaan kuitenkin korvata verkosta ladatuilla asetteluilla ja sivuilla.

Tässä esimerkissä malli määrittää yksinkertaisen rakenteen ja asetusjoukon verkosta ladattavan sisällön tekijöille. Ota huomioon, että jotkin sivun osat (tässä tapauksessa ylätunniste) on kokonaan määritetty ja lukittu mallissa. Verkosta tietoja lataavat tekijät eivät voi muuttaa niitä. Muut osat (tässä tapauksessa tekstiosa) voidaan määrittää verkosta tietoja lataaville tekijöille tiettyjen ohjeiden mukaisesti (tässä tapauksessa tietty vähimmäis- ja enimmäismäärä erilaisia moduuleja). Ja muut osat (tässä tapauksessa alatunniste) määritetään mallissa. Verkosta tietoja lataavat käyttäjät eivät voi korvata niitä.

Toimipaikan ja tuotemerkin hallinnoijien on tärkeää määrittää alussa oikea rajoituksen ja joustavuuden välinen tasapaino alitason asettelulle ja sivun tekijöille. Kun malleja käytetään, tämä tasapaino on täysin määritettävissä. Se vaikuttaa siihen, päivitetäänkö sivun elementit keskitetysti (lukittu mallissa) vai jätetäänkö ne yksittäisille alitasoille, jotka ovat alempana sivuhierarkiassa.

Lisätietoja mallien käyttämisen aloittamisesta on kohdassa [Mallien käsitteleminen](work-with-templates.md).

## <a name="layouts"></a>Asettelut

Asettelut ovat sivumallihierarkian seuraavalla tasolla mallien alla. Malli määrittää kaikki sivulla sallitut moduulit. Asettelu sen sijaan on moduulien täsmällinen valikoima ja järjestely. Sivut ovat sivumallihierarkian seuraavalla tasolla asettelujen alla. Ne määrittävät asettelussa valittujen moduulien lokalisoidun sisällön.

Seuraava esimerkki perustuu edellisen osan malliesimerkkiin. Siinä kerrotaan, miten perusasettelu määritetään seuraavalla tavalla:

- Asettelun päätason malli edellyttää, että tekstiosan säilö sisältää yhdestä kymmeneen moduulia. Moduuli voi olla vain hero-, ominaisuus-, karuselli tai ilmoituspalkkimoduuli. Tämän vuoksi asettelu voi määrittää moduulien seuraavan valinnan ja järjestelyn:

    - Tekstiosan säilön ensimmäinen moduuli on ilmoituspalkkimoduuli. Tämän jälkeen on hero-moduuli ja kaksi ominaisuusmoduulia.
    - Ensimmäinen ominaisuusmoduuli tasataan vasemmalle ja toinen ominaisuusmoduuli oikealle.

- Vaikka oletusalatunniste periytyy päämallilta, mallin tekijä jätti alatunnisteen lukitsematta. Tämän vuoksi asettelu voi korvata sen määrittämällä toisen alatunnisteen osan.

Tämän esimerkin asettelu määrittää alitason sivujen moduulien lopullisen järjestyksen. Mallin tavoin asettelussa voidaan määrittää moduulin oletusominaisuuksia tai lukittuja ominaisuuksia, jotka alitason sivut perivät aina (esimerkiksi ominaisuusmoduulien tasaus). Jokaisen asettelun moduulin todellinen sisältö tai todelliset tiedot määritetään tämän jälkeen alempana hierarkiassa jokaisen alitason sivun esiintymässä. Tärkeä ero on se, että asettelut eivät suoraan sisällä lokalisoitavaa sisältöä, vaan tämä sisältö on niiden alitason sivuilla. Asettelun ensisijainen tehtävä on määrittää sen alitason sivujen moduulien lopullinen järjestely ja oletusmääritys.

Tämä hierarkia on tehokas kahdesta syystä. Saman päämallin jakavia asetteluita kohdellaan yhteensopivina asettelua vaihtavien skenaarioiden kanssa. Tämän vuoksi minkä tahansa sivun asettelu voidaan vaihtaa toiseen saman mallihierarkian asetteluun ilman, että sivutason sisältöä tarvitsee muuttaa. Voit hyödyntää tätä ominaisuutta kausittaisissa suunnittelupäivityksissä, kokeiluissa ja sivuston pysyvissä muutoksissa. Asettelut tarjoavat myös toisen tavan muokata sivuryhmän jaettuja elementtejä keskitetysti ilman, että yksittäisiä sivuja on päivitettävä. Jos tuoteluokassa on esimerkiksi 1 000 sivua, jotka jakavat saman asettelun, asettelun moduulit voidaan järjestää uudelleen. Näin muutos vaikuttaa heti kaikkiin 1 000 alitason sivuun.

Tämän hierarkian avulla voit tarjota ketterän ja tehokkaan sivustorakenteen. Se säästää kustannuksia, on skaalautuva ja tuottaa parempia tuloksia, koska sivusto kehittyy koko ajan.

### <a name="preset-and-custom-layouts"></a>Esimääritetyt ja mukautetut asettelut

Sivuston asettelut voivat olla *esimääritettyjä* tai *mukautettuja*:

- **Esimääritetyt asettelut** mahdollistavat sivun luonnin työnkulun, jossa kaikki moduulit on jo valittu ja järjestetty ja vain tietojen syöttäminen on pakollista. Näin voidaan säästää aikaa, jos muokattavana on useita sivuja, joissa on samat asetteluvaatimukset. Esimääritetyillä asetteluilla on yksi moneen -suhde alitason sivujen kanssa. Näin ollen yhden esimääritetyn asettelun avulla voidaan keskitetysti ohjata satojen tai tuhansien alitason sivujen moduulijärjestystä.
- **Mukautetut asettelut** ovat pääasiassa kerran käytettäviä asetteluja, jotka on upotettu yhdelle sivulle. Niitä ei näytetä vaihtoehtona luotaessa uusia sivuja tai vaihdettaessa asettelun skenaarioita. Tämän menetelmän etu on se, että tekijä voi kokeilla mukautettua asettelua käyttävän sivun muokkaamista. Jos tekijä tämän jälkeen haluaa käyttää asettelua uudelleen muilla sivuilla, se voidaan muuntaa helposti esimääritetyksi asetteluksi. Uusi esimääritetty asettelu näytetään tämän jälkeen vaihtoehtona sivun luonnin työnkuluissa ja asettelun muutosskenaarioissa sivuilla, jotka ovat samassa mallihierarkiassa. Vastaavasti esimääritetyt asettelut voidaan haaroittaa mukautetuiksi asetteluiksi. Näin tekijä voi poistaa sivun esimääritetyistä asettelusta ja luoda uuden kerran käytettävän mukautetun asettelun. (Kaikki päätason mallin rajoitteet koskevat tätä uutta mukautettua asettelua.)

Esimääritettyjä ja mukautettuja asetteluja muokataan muokkaustyökalujoukon eri osissa. Koska mukautetuilla asetteluilla ei ole riippuvuuksia muilla sivuilla, niitä muokataan suoraan sivueditorissa. Tässä tapauksessa asettelun olemassaolo on useimmiten näkyvissä käyttäjälle. Se näytetään vain sivutason ominaisuuksissa ja asettelun vaihtoehtojen toiminnoissa. Koska esimääritettyjen asettelujen muutokset voivat vaikuttaa useisiin alitason sivuihin, niitä on muokattava asettelueditorissa. Siinä julkaisutoiminnoissa otetaan huomioon alitason sivujen kaikki vaikutukset verkosta ladattaviin tietoihin.

Seuraavissa kuvissa näkyvät esimääritettyjen ja mukautettujen asettelujen skenaariot.

![Esimääritetyt ja mukautetut asetteluskenaariot.](../commerce/media/template-figure1.png)

Lisätietoja esimääritettyjen asetteluiden käyttämisen aloittamisesta on kohdassa [Esimääritettyjen asetteluiden käyttäminen](work-with-layouts.md).

## <a name="additional-resources"></a>Lisäresurssit

[Mallien käyttö](work-with-templates.md)

[Esimääritettyjen asettelujen käyttö](work-with-layouts.md)

[Julkaisuryhmien kanssa työskenteleminen](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
