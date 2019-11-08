---
title: Resurssienhallinnan parametrit
description: Resurssien hallinnassa on määritettävä resursseihin, työtilauksiin ja työtilausten ajoitukseen liittyvät yleiset parametrit.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3ccbb7eed643abf613f8b75ae78854246d20f6d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569867"
---
# <a name="asset-management-parameters"></a>Resurssienhallinnan parametrit

[!include [banner](../../includes/banner.md)]

 

Resurssien hallinnassa on määritettävä resursseihin, työtilauksiin ja työtilausten ajoitukseen liittyvät yleiset parametrit. Tässä ohjeaiheessa käsitellään, kuinka voit määrittää nämä parametrit. Avaa lomake valisemalla **Resurssien hallinta** > **Asetukset** > **Resurssien hallinnan parametrit**.

**Ohjattu tietojen luonti**-painikkeen avulla voidaan luoda automaattisesti asetustietoja testi- tai esittelytarkoituksiin yrityksessä Dynamics 365 Supply Chain Managementissa. Lisätietoja ohjatun toiminnon käyttämisestä on kohdassa "Määritä resurssien hallinnan testitiedot".

**Resurssit**-linkki

- **Oletusarvoinen toiminnallinen sijainti** on toiminnallinen vakuisijainti, joka valitaan automaattisesti resursseille, kun luot uusia resursseja.  
- Valitse **Vakiokalenteri**-kentässä kalenteri, jota käytetään resurssin suorituskykyilmaisien laskemiseen, jos resurssille ei ole valittu resurssia.  
- Valitse **Näytä**-kentässä vakionäkymä, joka näytetään, kun avataan **Resurssinäkymä** -lomake (**Resurssien hallinta** > **Yhteiset** > **Resurssit** > **Resurssinäkymä**).
- **Oletuspyyntötyyppi** on huoltopyynnön vakiotyyppi, joka valitaan automaattisesti, kun luot uuden pyynnön.  
- Jos haluat luoda projekteja, jotka liittyvät resursseihin, projektin suhteet, kuten **Pääprojekti**, **Projektihierarkia** ja asetus **Luo projekteja automaattisesti** määritetään **Resurssien hallinnan parametrit** -osassa.  
- **Työtilauksen projektin peite** -kentässä määritetään työtilauksille ja aliresursseille sallittujen aliprojektien määrä. Työtilauksen peitteen avulla määritetään, kuinka monta työtilausta voidaan luoda resurssille ja miten sitä käytetään liittyvässä työtilaustyön projektissa. Työtilauksen peite määritetään **Liittyvän työtilauksen peite** -kentässä kohdassa **Resurssien hallinnan parametrit** (**Resurssien hallinta** > **Asetukset** > **Resurssien hallinnan parametrit** > **Työtilaukset**).  
>[!NOTE]
>Liittyvän työtilauksen peitteen muoto on useita hajautusmerkkejä (#) sen mukaan, kuinka paljon työtilauksia oletat luovasi resurssille. Esimerkki: ## sallii enintään 99 aliprojektin luonnin.  
- Työtyyppien ennusteet tallennetaan **Ennusteprojekti**-kentässä valittuun projektiin. Jokaiselle työtyypille luodaan automaattisesti uusi aktiviteetti ennusteprojektiin. Työtyypin ennusteet tallennetaan ennusteprojektiin.  
- Valitse **Malli**-kentässä projektityypissä ja työtilausennusteissa käytettävä ennustemalli.  


**Työtilaukset**-linkki

- **Työtilauksen oletustyyppi** määrittää vakioasetukset työtilausta luotaessa.  
- **Ennaltaehkäisevän työtilauksen tyyppi** määrittää työtilaustyypin, jota käytetään luotaessa työtilauksia ylläpitosuunnitelmista. Jos tämä kenttä jätetään tyhjäksi, työtilauksen tyypiksi käytetään **Työtilauksen oletustyyppi** -kenttän arvoa.  
- **Liittyvän työtilauksen peite** -kenttään määritetään työtilausten enimmäismäärä, joka voidaan liittää työtilaukseen. Esimerkki: ## sallii enintään 99 liittyvää työtilausta. Jos määrität peitettä tässä kuvatulla tavalla, siihen liittyvät työtilaukset numeroidaan [työtilauksen tunnus työtilaukselle, johon työtilaus liittyy]-01, -02, -03 ja niin edelleen. Jos tähän kenttään ei määritetä peitettä, liittyvä työtilaus saa seuraavan peräkkäisen työtilauksen tunnuksen.  
- Valitse "Kyllä" **Kopioi viat** -vaihtopainikkeesta, jos haluat kopioida työtilauksiin rekisteröidyt viat automaattisesti liittyviin ylläpitopyyntöihin.  
- **Taso**-kentässä määritetään toiminnallinen sijaintitaso, joka lisätään työtilaukseen automaattisesti, jos kaikki liittyvät työtilaustyöt viittaavat samaan toiminnalliseen sijaintiin. Jos työtilauksen työt eivät kaikki liity määritettyyn tasoon samassa toiminnallisessa sijainnissa, työtilauksen **Toiminnallinen sijainti** -kenttä jätetään tyhjäksi. Esimerkki: Jos lisäät tähän kenttään numeron "1", se on toiminnallisen sijainnin rakenteen ylin taso. Jos lisäät tähän kenttään numeron "0", et ole määrittänyt tiettyä toiminnallista sijaintitasoa, vain, että työtilauksen kaikkien työtilaustöiden on oltava yhteydessä samaan toiminnalliseen sijaintiin, jolle kyseinen toiminnallinen sijainti lisätään työtilaukseen.  
- Työtilauksen kulutuksen kirjaamisen yhteydessä käytettävät kirjauskansiot voidaan valita**Yleiset**-pikavälilehden **Tunti**-, **Nimike**- ja **Kulu**-kentissä.  
- Valitse **Tuotteen kielen lähde** -kentässä, mitä kieltä käytetään resurssien hallinnan raporttien tuotenimissä. Voit valita yrityksen tilille määritetyn kielen tai tällä hetkellä kirjautuneena olevalle käyttäjälle määritetyn kielen.  
- Valitse "Kyllä" **Reaaliaikainen päivitys** vaihtopainikkeesta, jos haluat päivittää automaattisesti muutokset työtyypin oletusarvoihin, ylläpitosuunnitelmiin ja ylläpitokierroksiin.
> - Jos valitset "Ei", muutoksia työtyypin oletuksiin, ylläpitosuunnitelmiin ja ylläpitokierroksiin ei päivitetä automaattisesti resurssien hallinnassa.  
> - Valitse vaihtopainikkeesta "Ei", jos synkronoitavia tietoja on paljon, esimerkiksi useita resursseja tai toiminnallisia sijainteja, jotka on määritetty huoltosuunnitelmille tai huoltokierroksille, tai suuri määrä ylläpitosuunnitelmia tai -kierroksia.  
> - Jos teet muutoksia työtyypin oletusarvoihin tai ylläpitosuunnitelmiin tai ylläpitokierroksiin ja olet valinnut "Ei" reaaliaikaiseen päivitykseen, varoitus ei välttämättä näy, jos muutokset vaikuttavat seuraaviin:
>   - Kunnossapitosuunnitelmille tai -kierroksille asetetut toiminnalliset sijainnit  
>   - Kunnossapitosuunnitelmille tai -kierroksille asetetut objektit  
>   - ylläpitosuunnitelmien määritykset  
>   - ylläpitokierrosten määritykset  
- **Luokka**-pikavälilehdessä voidaan määrittää työtilausten kulutukseen liittyvät oletusluokat.  


**Työtilausten ajoitus** -linkki

- **Ajoituksen aikaraja** määrittää jakson päivinä (laskettu työtilauksen odotetusta alkamispäivämäärästä), jonka aikana työtilauksen työt suunnitellaan.  
- **Pääsuunnitelma** liittyy **Organisaation hallinto** -moduulin resursseihin. Jos valitset pääsuunnitelman tässä kentässä, voit tarkastella työtilauksiin liittyviä kapasiteettivarauksia kohdassa **Kapasiteettivaraukset** (**Organisaation hallinto** > **Resurssit** > **Resurssit** > valitse resurssi > **Resurssi**-välilehti > **Kapasiteettivaraukset**-painike). Jos jätät tämän kentän tyhjäksi, voit tarkastella työtilauksiin liittyviä kapasiteettikuormituksia kohdassa **Kapasiteetin kuormitus** (**Organisaation hallinto** \> **Resurssit** \> **Resurssit** \> valitse resurssi \> **Resurssi**-välilehti \> **Kapasiteetin kuormitus** -painike).  

>[!NOTE]
>Valinta, joka koskee pääsuunnitelman käyttämistä **Resurssien hallinta** -moduulissa, ja siihen liittyvä lomake, jota käytetään saamaan yleiskatsaus kapasiteettivarauksista tai kapasiteetin kuormituksesta, on vakioasetus. **Pääsuunnitelma**-kentän asetuksista riippuen voit käyttää kapasiteettitietoja joko **Kapasiteettivaraukset**- tai **Kapasiteetin kuormitus** -osassa **Organisaation hallinta** -moduulissa. Ei ole mahdollista luoda asetuksia, joissa molemmissa näkymissä näkyvät kapasiteettivaraukset.  

Alla olevassa luettelomerkkiluettelossa olevat kentät liittyvät laskettuihin luokituspisteisiin, joita käytetään työtilauksen prioriteetin laskemiseen työtilauksen ajoituksessa.

- **Prioriteetti** – luokituspisteet lasketaan yhdessä **Kriittisyys** -ja **Alkamispäivämäärä** -kenttien luokituspisteiden kanssa. Tämän kentän numero jaetaan työtilauksen **Prioriteetti-**-kentän numerolla. Esimerkki: Jos tähän kenttään lisätään arvo "5,00" ja työtilaukselle on asetettu prioriteetti "20", prioriteetin luokituspisteet ovat 0,25.  
- **Kriittisyys** – luokituspisteet lasketaan yhdessä **Prioriteetti** -ja **Alkamispäivämäärä** -kenttien luokituspisteiden kanssa. Tämän kentän numero kerrotaan työtilauksen **Kriittisyys**-kentän numerolla. Esimerkki: Jos tähän kenttään lisätään arvo "10,00" ja työtilaukselle on asetettu kriittisyys "5", prioriteetin kriittisyyspisteet ovat 50.  
- **Alkamispäivämäärä** – luokituspisteet lasketaan yhdessä **Prioriteetti** -ja **Kriittisyys** -kenttien luokituspisteiden kanssa. Tämä kenttä ilmaisee päivittäisen tuloksen negatiivisena arvona, ja sitä verrataan työtilauksen **Odotettu alkamispäivämäärä** -kenttään. Esimerkki: Jos tähän kenttään lisätään arvo "10,00" ja työtilauksen odotettu alkamispäivä on kolme päivää tästä lähtien, luokittelun tulos on miinus 30,00. Edellä kuvattujen esimerkkien **Prioriteetti**- ja **Kriittisyys**-kenttien tuloksien 0,25 ja 50 lisääminen tuottaa arvon plus 20,25. Tätä lukua verrataan kaikkien muiden työtilausten luokituspisteisiin, ja korkeimmat luokituspisteet suunnitellaan ensin.  
- **Vastuullinen työntekijä** -luokituspisteet lasketaan yhdessä **Vastuullinen työntekijäryhmä**-, **Ensisijainen työntekijä**-, **Ensisijainen työntekijäryhmä**-, **Resurssin sijainti**- ja **Aloituspäivämäärä** -luokituspisteiden arvojen kanssa. Jos tähän kenttään lisätään arvo "50,00" ja työtilaukselle on valittu vastuullinen työntekijä, työntekijä saa 50 pistettä työntekijän kokonaislaskennassa työtilausten ajoituksessa.  
- **Vastuullinen työntekijäryhmä** -luokituspisteet lasketaan yhdessä **Vastuullinen työntekijä**-, **Ensisijainen työntekijä**-, **Ensisijainen työntekijäryhmä**-, **Resurssin sijainti**- ja **Aloituspäivämäärä** -luokituspisteiden arvojen kanssa. Jos tähän kenttään lisätään arvo "50,00" ja työtilaukselle on valittu vastuullinen työntekijä, työntekijä saa 50 pistettä työntekijän kokonaislaskennassa työtilausten ajoituksessa.  
- **Rajoita vastuullisiin** -vaihtopainike (kyllä/ei) rajoittaa työtilausten suunnittelussa käytettävissä olevien työntekijöiden määrää. Valitse "Ei", jos haluat laskea kaikkien työntekijöiden pisteet riippumatta siitä, onko ne määritetty vastuullisiksi työntekijöiksi vai vastuullisen työntekijäryhmän jäseneksi. Valitse "Kyllä", jos haluat laskea työtilauksen vastuulliseksi työntekijäksi määritettyjen työntekijöiden pisteet ja/tai jos ne sisältyvät työtilauksessa valittuun vastuutyöntekijäryhmään.  
- **Ensisijainen työntekijä** -luokituspisteet lasketaan yhdessä **Vastuullinen työntekijä**-, **Ensisijainen työntekijä**-, **Ensisijainen työntekijäryhmä**-, **Resurssin sijainti**- ja **Aloituspäivämäärä** -luokituspisteiden arvojen kanssa. Neljä luokituspistettä lasketaan ja lisätään yhdessä, jotta voidaan valita, mikä työntekijä määritetään mihinkin työtilaukseen ajoittamisen yhteydessä. Jos tähän kenttään lisätään arvo "10,00" ja työtilaukselle on valittu ensisijainen työntekijä, työntekijä saa 10 pistettä työntekijän kokonaislaskennassa työtilausten ajoituksessa.  
- **Ensisijainen työntekijäryhmä** -luokituspisteet lasketaan yhdessä **Vastuullinen työntekijä**-, **Ensisijainen työntekijä**-, **Ensisijainen työntekijäryhmä**-, **Resurssin sijainti**- ja **Aloituspäivämäärä** -luokituspisteiden arvojen kanssa. Jos tähän kenttään lisätään arvo "10,00" ja työtilaukselle valittuun ensisijaiseen työntekijätyhmään on määritetty työntekijä, työntekijä saa 10 pistettä työntekijän kokonaislaskennassa työtilausten ajoituksessa.  
- **Rajoita ensisijaisiin** -vaihtopainike (kyllä/ei) rajoittaa työtilausten suunnittelussa käytettävissä olevien työntekijöiden määrää. Valitse "Ei", jos haluat laskea kaikkien työntekijöiden pisteet riippumatta siitä, onko ne määritetty ensisijaisiksi työntekijöiksi vai ensisijaisen työntekijäryhmän jäseneksi. Valitse "Kyllä", jos haluat laskea vain niiden työntekijöiden pisteet, jotka on määritetty ensisijaisiksi työntekijöiksi ja/tai ensisijaisen työntekijäryhmän jäseneksi.  
- **Sijainti** -luokituspisteet lasketaan yhdessä **Vastuullinen työntekijä**-, **Ensisijainen työntekijä**-, **Ensisijainen työntekijäryhmä**-, **Resurssin sijainti**- ja **Aloituspäivämäärä** -luokituspisteiden arvojen kanssa. Jos tähän kenttään lisätään arvo "3 000,00", työntekijä saa 3 000 pistettä laskennassa, jos työntekijä sijaitsee samassa tehtaassa tai laitoksessa kuin resurssi, jolle työ ajoitetaan.  

  - Jos yrityksessä käytetään toiminnallisia sijainteja, työntekijät saavat täydet pisteet, jos ne sijaitsevat resurssiin liittyvässä toiminnallisessa sijainnissa. Jos resurssin toiminnallisella sijainnilla on pääresurssi, kyseisen toimintasijainnin työntekijät saavat puolet pisteistä. Jos kyseisessä sijainnissa on myös ylätaso, kyseisessä sijainnissa olevat työn tekijät saavat 1/3 pisteistä. Jos kyseisessä sijainnissa on myös ylätaso, kyseisessä sijainnissa olevat työn tekijät saavat 1/4 pisteistä jne.  
  - Jos yrityksessä käytetään resurssin sijaintia, jota ei suositella, sijaisntipisteet lasketaan sijainnin, alueen ja vyöhykkeen mukaan. Työntekijät saavat täydet pisteet, jos ne sijaitsevat resurssiin liittyvässä sijainnissa ja alueella sekä vyöhykkeellä. Jos työntekijän sijainti vastaa vain sijaintia ja aluetta, työntekijän luokituspisteet ovat 2/3 täysistä pisteistä. Jos työntekijän sijainti vastaa vain sijaintia, työntekijän luokituspisteet ovat 1/3 täysistä pisteistä.  

- **Rajoita sijainteihin** -vaihtopainike (kyllä/ei) rajoittaa työtilausten suunnittelussa käytettävissä olevien työntekijöiden määrää. Valitse "Ei", jos haluat laskea kaikkien työntekijöiden pisteet kaikkien toiminnallisten sijaintien osalta. Valitse "Kyllä", jos haluat laskea vain niiden työntekijöiden pisteet, jotka on liitetty työtilauksen toiminnalliseen sijaintiin.

>[!NOTE]
>Kolme Rajoita... -vaihtopainiketta käytetään työtilausten ajoittamisen nopeuttamiseen rajoittamalla työntekijöille laskettujen tulosten määrää.

**Työntekijän aloituspäivämäärä** -luokituspisteet lasketaan yhdessä **Vastuullinen työntekijä**-, **Ensisijainen työntekijä**-, **Ensisijainen työntekijäryhmä**-, **Resurssin sijainti**- ja **Aloituspäivämäärä** -luokituspisteiden arvojen kanssa. Tämä kenttä ilmaisee päivittäisen tuloksen negatiivisena arvona, ja sitä verrataan työtilauksen **Odotettu alkamispäivämäärä** -kenttään. Jos tähän kenttään lisätään arvo "10,00" ja työtilauksen odotettu alkamispäivä on huomenna, luokittelun tulos on miinus 10,00.

  - Olettaen, että ajoitettavassa työtilauksessa ei ole valittu vastuullista työntekijää tai vastuullista työntekijäryhmää, ja lisätään ja vähennetään esimerkkien luokituksen pistearvot **Ensisijainen työntekijä**-, **Ensisijainen työntekijäryhmä**-, **Resurrsin sijainti**- ja **Alkamispäivämäärä**-kentissä, saat yhteensä summan 3 010,00. Tämä tarkoittaa korkeaa pistemäärää työntekijälle, joka on jo valittu ensisijaiseksi työntekijäksi, sekä kuuluu työtilauksen ensisijaiseen työntekijäryhmään, ja työntekijä myös sijaitsee samassa laitoksessa kuin resurssi, jolle työ on aikataulutettava. Kaiken kaikkiaan tämä tarkoittaa, että on hyvin mahdollista, että kyseinen työntekijä valitaan työn suorittamiseen työtilauksen ajoituksessa.  
  - Jos arvo "0,00" lisätään johonkin edellä mainituista kahdeksasta kentästä, luokituspisteet eivät ole käytössä työtilausten ajoituksessa.  


**Tiedostotyypit**-linkki

Valitse tiedostotyypit, joita voidaan käyttää työtilausraporttiin liittyvien liitteiden tulostamiseen. Tämä tehdään napsauttamalla tiedostotyyppiä **Saatavilla**-osassa ja napsauttamalla ![eteenpäin osoittavaa nuolta](media/15-setup-for-objects.png). Jos haluat poistaa valitun tiedostotyypin, valitse tiedostotyyppi **Valittu**-osassa ja napsauta ![takaisin-nuolta](media/16-setup-for-objects.png).



**Numerosarjat**-linkki

Valitse tässä osassa tarvittavat numerosarjat. Resursseille on kaksi numerosarjaa: yksi manuaalisesti luoduille resursseille ja toinen odottavien resurssien kautta luoduille resursseille.
