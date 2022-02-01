---
title: Standardikustannuksen muuntamisen yleiskuvaus
description: Tässä artikkelissa kuvataan prosessia, jonka avulla määritetään ja suoritetaan standardikustannusmuunto. Luetellut vaiheet suoritetaan sen jälkeen, kun standardikustannusmuunnon edellytykset ovat täyttyneet.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "78212"
- intro-internal
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9796449bee4361b2b871af10d30341c2f0760ab1
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982686"
---
# <a name="standard-cost-conversion-overview"></a>Standardikustannuksen muuntamisen yleiskuvaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan prosessia, jonka avulla määritetään ja suoritetaan standardikustannusmuunto. Luetellut vaiheet suoritetaan sen jälkeen, kun standardikustannusmuunnon edellytykset ovat täyttyneet. 

**Standardikustannusmuunnot**-sivun avulla voit muuntaa valittujen nimikkeiden erän varastomallin todellisesta kustannuslaskelmasta standardikustannuslaskelmaksi. Muuntoprosessi käsittää varaston sulkemisen, useita siirtojakson (siirron alkamispäivämäärän ja suunnitellun muuntopäivämäärän välinen aika) aikana tehtäviä vaiheita, muunnon suorituksen sekä liittyvän varaston sulkemisen.

-   Varaston sulkeminen ennen siirtojaksoa − Varaston sulkeminen on edeltävä vaihe, koska se täsmäyttää nimikkeen avoimet tapahtumat vanhalla arvostusmenetelmällä. Siirtojakson aikana voit syöttää ja kirjata takautuvia tapahtumia (kuten laskuja) niin, että voit sulkea edellisen jakson. Varaston sulkemispäivämäärän on oltava yhtä päivää ennen siirron alkamispäivämäärää, jolloin vanhan varaston arvostusmenetelmän käyttö voidaan lopettaa oikein.
-   Muunnon vaiheet siirtojakson aikana – **Standardikustannusmuunnot** -sivun avulla voit luoda muuntotietueen, joka sisältää myös uuden kustannuslaskentaversion käyttäjän määrittämän tunnisteen. Voit määrittää muunnettavat nimikkeet ja syöttää nimikkeen odottavat standardikustannukset (juuri luodussa kustannuslaskentaversiossa). Suorita valittujen nimikkeiden tarkistus ja määritä mahdolliset muunnon estävät ongelmat. Ratkaise ongelmat ennen toisen tarkistuksen suoritusta. Kun nimikkeet läpäisevät tarkistukset, voit muuttaa (muuntotietueen) tilaksi **Valmis**. Suorita muunto suunniteltuna muuntopäivänä ja sulje varasto halutessasi. Nimikkeen varaston siirtotapahtumat kirjataan ja arvostetaan vanhan varastomallin mukaan siirtojakson aikana. Ne uudelleenarvostetaan standardikustannusten mukaan onnistuneen muunnon jälkeen.
-   Varaston sulkeminen ennen muuntoa − Varaston sulkeminen voidaan sisällyttää osaksi muuntoa suunniteltuna muuntopäivänä. Se voidaan suorittaa myös erillisenä vaiheena etukäteen.

Muuntoprosessin onnistuneen suorituksen jälkeen jokaisella nimikkeellä on standardikustannusvarastomalli ja nimikkeen standardikustannukset ovat käytössä. Seuraavat varastotapahtumat arvostetaan nimikkeen standardikustannusten mukaan. Lisäksi järjestelmä muuntaa nimikkeen varastotilannetapahtumat vastaanotoiksi ja varastostaotot standardikustannuksiksi muuntopäivämäärän mukaan. Järjestelmä muuntaa myös nimikkeen kirjanpidon käytettävissä olevan varaston standardikustannuksiksi ja kirjaa arvoeron varaston uudelleenarvostukseksi. Kaikki muunnon jälkeiset tapahtumat arvostetaan nimikkeen standardikustannusten kanssa. Et voi syöttää takautuvia tapahtumia ennen muuntopäivää, koska varaston sulkeminen on suoritettava päivää ennen muuntopäivää. Muunto voidaan suorittaa siis vain siinä tapauksessa, että varaston sulkeminen on tehty päivää ennen. Tätä varaston sulkemista ei voi peruuttaa.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Määritä standardikustannusmuunnon tietue ja liittyvä kustannuslaskelmaversio.
Luo muuntotietue **Standardikustannusmuunnot**-sivulla. Uusi muuntotietue voidaan luoda vain, jos aiemmin luodut muuntotietueet ovat valmiit. Siirron alkamispäivä ja suunniteltu muuntopäivä määrittävät suunnitellun siirtojakson keston. Suunniteltu siirtojakso voi olla yhdenkin päivän pituinen. Suunnitellun siirtojakson tarkoitus on tarjota riittävästi aikaa muuntoprosessin monien vaiheiden suoritukselle. Varaston sulkeminen on suoritettava päivää ennen siirtojakson alkamispäivää. Tällöin täsmäytykset ovat valmiit ennen muuntoprosessin alkua. Voit muuttaa siirtojakson alkupäivämäärää niin, että se on varaston sulkemista seuraavana päivänä tai suorittaa varaston sulkemisen niin, että päivämäärät ovat peräkkäiset. Kun syötät tietoja muuntotietueeseen, syötät myös uuden kustannuslaskelmaversion käyttäjän määrittämän tunnuksen, joka sisältää muunnettujen nimikkeiden standardikustannukset. Muuntotietueen tietojen tallentaminen luo automaattisesti kustannuslaskelmaversion.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. Tarkista ja muokkaa muuntotietueen uutta kustannuslaskelmaversiota
Uusi kustannuslaskelmaversio on kohdistettu muuntotietueeseen **muunnoksen** kustannuslaskelmatyypin mukaan. Kohdistettu kustannuslaskelmaversio toimii standardikustannusten kustannuslaskelmaversiona. Se sisältää muuntotietueeseen liittyvien nimikkeiden kustannustietueet. Muuntotietueen kohdistetulla kustannuslaskentaversiolla on seuraavat ominaisuudet, jotka tulee tarkistaa ja joita tulee muuttaa tarvittaessa.

-   **Kustannuslaskentatyyppi:** Tämän kentän arvoksi pitää määrittää **Standardikustannus**.
-   **Versio:** Tunnus määrittää tiedot, jotka kustannuslaskelmaversion tunnuksen muuntotietueeseen on syötetty.
-   **Nimi:** Oletusarvon mukaan nimi on tyhjä. Voit halutessasi antaa nimen.
-   **Esto:** Tämän kentän arvoksi on määritettävä **Ei**. Voit syöttää kustannustietueita kustannuslaskelmaversioon siihen asti kunnes muuntotietueen tilaksi muutetaan **Valmis**. Tila **Valmis** tarkoittaa, että valitut nimikkeen on tarkistettu ja kustannustietueiden muutoksia ei enää tule sallia.
-   **Estä aktivointi:** Tämän kentän arvoksi on määritettävä **Kyllä**. Et voi aktivoida manuaalisesti odottavaa kustannustietuetta, johon on kohdistettu kustannuslaskelmaversio. Aktivointi suoritetaan, kun suoritat muunnon.
-   **Päivämäärästä:** Aloituspäivä viittaa muuntotietueelle syötettävään suunniteltuun muuntopäivään.
-   **Toimipaikka:** Jätä tämä kenttä tyhjäksi, jotta kustannustietueita voi lisätä kaikille toimipaikoille.
-   **Salli hintatyyppi -kenttäryhmä:** Määritä tämän kentän arvoksi **Kyllä**, jotta vain kustannushintatietueita voi syöttää.
-   **Varmistusperiaate:** Tämän kentän arvoksi on määritetty **Ei mitään**. Vaihda varmistusperiaatteeksi **Aktiivinen**, jos tarvitset toisissa kustannuslaskentaversioissa aktivoituja kustannustietoja. Voit esimerkiksi tarvita tietoja komponenteista, kustannusluokista ja epäsuorista kustannuksista valmistettujen nimikkeiden kustannusten laskentaa varten.
-   **Varakustannuslaskentaversio:** Jätä tämä kenttä tyhjäksi.

Kohdistetun kustannuslaskelmaversion kustannustietoja voi ylläpitää vain **Standardikustannusmuunnot**-sivulla. Et voi käyttää kohdistetun kustannuslaskelmaversion kustannusten syöttöön tai laskentaan muunnon aikana **Kustannuslaskentaversion määritys** -sivua tai **Kustannuslaskentaversion ylläpito** -sivua. Näitä sivuja voi kuitenkin käyttää kohdistetun kustannuslaskelmaversion ylläpitoon muunnon suorituksen jälkeen.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. Määritä standardikustannuksiin muunnettavat nimikkeet
Määritä yksittäiset standardikustannuksiksi muunnettavat nimikkeet **Standardikustannusmuunnot**-sivun avulla. Voit lisätä useita nimikkeitä **Lisää nimikkeitä standardikustannusmuuntoon** -sivun avulla. Tavallisesti kaikki valmistetut nimikkeet sisällytetään yhteen muuntotietueeseen, jolloin kustannukset lasketaan oikein.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. Syötä tai laske jokaiselle muunnettavalle nimikkeelle odottavat standardikustannukset
Syötä ostettujen nimikkeiden ja siirtonimikkeiden kohdistetun kustannuslaskentaversion odottavat standardikustannukset **Nimikkeen hinta** -sivun avulla. Kustannustietueet ovat toimipaikkakohtaisia. Jokaiselle toimipaikalle on syötettävä nimikkeen odottavat kustannukset. Laske valmistettujen nimikkeiden odottavat standardikustannukset **Nimikkeen hinta** -sivun avulla. Jokaisen valmistavan toimipaikan valmistetun nimikkeen odottavat kustannukset on laskettava, ellei toimipaikka edusta siirtotoimipaikkaa. Tällöin odottavat kustannukset on syötettävä manuaalisesti. Joillakin nimikkeillä voi olla värin, koon tai konfiguraation tuotedimensio. **Standardikustannusmuunnot**-sivun **Käytä kustannushintaa variantin mukaan** -valintaruutu näyttää standardikustannukset jokaiselle tuotedimension yhdistelmälle. Kun tämän valintaruudun valinta poistetaan, sinun on syötettävä vain nimikkeen odottavat kustannukset.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. Tarkista ja ratkaise kaikki muunnettavien nimikkeiden ongelmat
Voit määrittää muunnettaviin nimikkeisiin liittyvät tunnistusongelmat **Standardikustannusmuunnon tarkistukset** -raportin avulla. Jos nimikkeeseen ei liity ongelmia, sen tilaksi muutetaan muunnostietueessa **Tarkistettu**. Jos nimikkeeseen liittyy ongelmia, ne on ratkaistava. Tämän jälkeen raportti suoritetaan uudelleen, kunnes tilaksi muutetaan **Tarkistettu**. Jos et voi ratkaista nimikkeen ongelmia ajoissa, voit poistaa nimikkeen muuntotietueesta ja muuntaa nimikkeen myöhemmin.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Muuta muuntotietueen tilaksi Valmis
Kun muuntotietueen tilaksi muutetaan **Valmis**, lopullinen tarkistus suoritetaan ennen standardikustannusmuunnon suoritusta. Tilaksi muutetaan **Valmis** vain, kun seuraavat ehdot täyttyvät:

-   Jokaisen muuntotietueen nimikkeen tila on **Tarkistettu**.
-   Varaston sulkeminen on suoritettu päivää ennen siirron aloituspäivää. Voit muuttaa siirtojakson alkupäivämäärää niin, että se on varaston sulkemista seuraavana päivänä tai suorittaa varaston sulkemisen niin, että päivämäärät ovat peräkkäiset.

## <a name="7-back-up-the-database-before-conversion"></a>7. Varmuuskopioi tietokanta ennen muunnosta
Varmuuskopioinnin avulla voit palauttaa tietokannan, jos muuntoprosessissa tapahtuu virheitä.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Suorita muunto, kun muuntotietueen tila on Valmis
Muuntoprosessi vaatii, että varaston sulkeminen suoritetaan päivää ennen suunniteltua muuntopäivää. Tämä vaatimus varmistaa sen, että takautuvia tapahtumia ei voi syöttää siirtojakson aikana. Jos varaston sulkemista ei ole vielä suoritettu, järjestelmä kysyy, haluatko suorittaa sen muuntoprosessin osana. Muuntoprosessi käsittelee yhdelle nimikkeelle kerrallaan. Ensimmäisenä käsitellään tuoterakenteen alimman tason nimikkeet (perustuu nimikkeen alatason koodiin). Nimikkeen tilaksi tulee onnistuneen muunnon jälkeen **Muunnettu**. Jos muuntoprosessi keskeytyy, muuntamattomien nimikkeiden tila on edelleen **Tarkistettu**. Muuntoprosessin onnistuneella suorituksella on seuraavia vaikutuksia:

-   Muuntotietueen tila muuttuu tilasta **Valmis** tilaksi **Päätetty**. Kunkin valitun nimikkeen tila muuttuu tilasta **Tarkistettu** tilaksi **Muunnettu**.
-   Muunnettujen nimikkeiden nimikemalliryhmä on muuttunut niin, että se heijastaa uutta standardikustannusvarastomallin ryhmää.
-   Muunnettujen nimikkeiden standardikustannukset on otettu käyttöön kohdistetussa kustannuslaskelmaversiossa.
-   Kustannuslaskelmaversion kustannustyyppi muuttuu tyypistä **Muunto** tyypiksi **Standardikustannus**. Kustannuslaskelmaversio toimii tämän jälkeen kuten mikä tahansa standardikustannusten kustannuslaskelmaversio.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. Tarkista ja täsmäytä muunnettujen nimikkeiden varaston arvot
**Varianssianalyysitiedot**-raportin avulla voit analysoida uudelleenarvostuksen varianssin. **Varaston arvo** -raportin avulla voit tarkastella varaston arvoa tiettynä päivämääränä.

-   Analysoi uudelleenarvostuksen varianssit. **Varianssianalyysitiedot**-raportin avulla voit tarkastella muunnettujen nimikkeiden varaston uudelleenarvostuksen variansseja. Myös **Vakiokustannustapahtumat**-sivun avulla voit tarkastella muunnettujen nimikkeiden varaston uudelleenarvostustapahtumia.
-   Analysoi varaston arvo ennen siirron aloituspäivää. **Varaston arvo** -raportin avulla voit tarkastella muunnettujen nimikkeiden varaston arvoja. Käytä raportin päättymispäivänä päivämäärää, joka on yhtä päivää ennen siirron aloituspäivää.
-   Analysoi varaston arvo ennen muuntopäivää. **Varaston arvo** -raportin avulla voit tarkastella muunnettujen nimikkeiden varaston arvoja. Käytä raportin päättymispäivänä päivämäärää, joka vastaa yhtä päivää ennen muuntopäivää.
-   Analysoi varaston arvo muuntopäivänä. **Varaston arvo** -raportin avulla voit tarkastella varaston arvoja muuntopäivänä. Sekä raportin aloitus- että lopetuspäivämäärä on vastattava muuntopäivää. Raportin valintaehdot vastaavat muunnettuja nimikkeitä.
-   Analysoi takautuvat varaston siirtotapahtumat. **Varaston arvo** -raportin avulla voit tarkastella muunnon jälkeen syötettyjä takautuvia varaston siirtotapahtumia. Käytä aloitus- ja lopetuspäivissä raporttiasetuksia niin, että ne vastaavat siirron aloituspäivää ja muuntopäivää vähennettynä yhdellä päivällä. Raportin valintaehdot vastaavat muunnettuja nimikkeitä. Raportti näyttää varaston siirtotapahtumat, jotka on tehty standardikustannuksina siirtojakson aikana.


## <a name="additional-resources"></a>Lisäresurssit

[Standardikustannuksen muuntamisen edellytykset](prerequisites-standard-cost-conversion.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]