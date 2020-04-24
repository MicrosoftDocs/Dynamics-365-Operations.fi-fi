---
title: Kaavat ja kaavaversiot
description: Tässä aiheessa on tietoja resepteistä ja reseptiversioista. Resepti määrittää prosessituotannon prosessiin kuuluvat materiaalit, valmistusaineet ja tulokset. Reseptejä käytetään tuotteiden suunnitteluun ja valmistamiseen prosessituotannossa.
author: cvocph
manager: tfehr
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a67fa0409226432d2068c7ed4f6a876a9278d365
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202051"
---
# <a name="formulas-and-formula-versions"></a>Kaavat ja kaavaversiot

[!include [banner](../includes/banner.md)]

Resepti määrittää prosessituotannon prosessiin kuuluvat materiaalit, valmistusaineet ja tulokset. Resepti ja sitä vastaava reitti määrittävät koko prosessin prosessituotannossa. Reseptejä käytetään tuotteiden suunnitteluun ja valmistamiseen prosessituotannossa.

Resepti koostuu ainesosista ja määristä, jotka tarvitaan tuottamaan tietty määrä reseptinimikettä. Voit käyttää reseptitoiminnallisuutta Varastonhallinnasta tai Tuotetietojen hallinnasta, riippuen suoritettavasta tehtävästä.

## <a name="formulas-and-formula-lines"></a>Reseptit ja reseptirivit
Resepti koostuu yhdestä tai useasta reseptirivistä, joilla tunnistetaan reseptiin kuuluvia ainesosia tai nimikkeitä. Reseptirivi voi sisältää tuoterakenteen nimikkeitä, reseptinimikkeitä, todellisen painon nimikkeitä, ostettuja nimikkeitä, oheistuotteita tai sivutuotteita. Koska monia nimikkeitä käytetään useissa tuotteissa, voit käyttää nimikettä useammassa kuin yhdessä reseptissä.

Esimerkkinä reseptistä annetaan suklaakeksi. Tämän reseptin ainesosat käyttävät useita rivejä, kuten jauho, sokeri, kananmunat, voi ja suklaahiput. Suklaakeksiesimerkissä on ainesosia, joita lähes varmasti käytetään muissa valmistusohjetyyppisissä resepteissä. Kun suklaakeksejä valmistetaan, valmistamisesta voi jäädä tähteitä, kuten muruja, tai jotkut kekseistä voivat palaa tai jäädä raa'aksi. Nämä nimikkeet voidaan määrittää oheistuotteiksi tai sivutuotteiksi tuotannon työvaiheiden mukaan.

Kun luot reseptirivin, rivityyppi määrittää, miten järjestelmä käsittelee rivin, kun suoritat pääsuunnittelun ja luot erätilauksia. Tulos on erilainen jokaisen rivin kohdalla. Erilaiset, valittavana olevat rivityypit esitellään seuraavassa taulukossa. 

| Rivilaji     | kuvaus  |
|---------------|--------------|
| Nimike          | Valitse **Nimike** kun nimike on raakamateriaalia tai puolivalmis nimike, joka on keräilty varastosta tai nimike on huollossa. |
| Haamu       | Valitse **Haamu**, kun haluat purkaa minkä tahansa alemman tason reseptinimikkeen, joka sisältyy reseptiriveille. Kun laadit erätilauksen arviota ja reseptin on hajotettu, komponenttinimikkeet luetellaan erätilauksen reseptiriveinä. Lisäksi tuotantoreititykseen lisätään vastaavat reititykset. Reseptinimikkeet puretaan nykyisen konfiguraation avulla. Kun käytät **haamurivityyppiä**, voit käsitellä reseptin eri tasoilla tapahtuvia tuotannon ja mittauksen konfiguraatioita. Jos valitset tuotteelle **Haamu**-tyypin **Vapautetun tuotteen tiedot** -sivun **Suunnittele**-pikavälilehdessä, ja käytät sitten tuotetta reseptissä, reseptirivin rivityypiksi muutetaan **Haamu**. **Haamu**-tyyppiä ei voi valita todellisen painon nimikkeelle tai nimikkeille, joiden tuotantolaji on **oheistuote**, **sivutuote**, tai **suunnittelunimike**. |
| Tarvekohdistuksen tarjonta | Valitse **Tarvekohdistuksen tarjonta** erätilauksen, tuotantotilauksen, kanbanin, siirtotilauksen tai ostotilauksen luomiseksi ainesosalle, joka on reseptirivillä. Liittyvä tilaus perustuu tilauksen oletusasetuksiin ja ainesosan tuotantotyyppiin, ja se luodaan kun erätilauksen arvio luodaan. Erätilaukselle varataan automaattisesti pakolliset ainesosamäärä. |
| Toimittaja        | Valitse **Toimittaja**, jos tuotantoprosessi käyttää alihankkijaa ja haluat luoda alihankkijalle osatuotannon tai ostotilauksen. Alihankkijan suorittama palvelu tai työ on luotava resepti- tai palvelunimikkeenä. Voit liittää sen nimikkeeseen reseptirivinä. Reititykseen on sisällyttävä työvaihe, joka on liitetty alihankkijan operatiivisiin resursseihin. Tämä työvaihe on liitettävä reseptiriviin kentän **Työvaihenro** avulla. |

## <a name="formula-versions"></a>Kaavaversiot
Kun luot uuden reseptin, sinun on ensin luotava reseptiversio ennen kuin lisäät reseptirivin nimikkeet ominaisuuksineen. Jokaisella reseptillä on oltava ainakin yksi versio. Reseptiversion **Hyväksytty**-painike on käytettävissä vasta, kun versiotietue on tallennettu. Kunkin reseptiversion tietue on liitetty vähintään yhteen oheis- tai sivutuotteeseen, jotka voidaan tuottaa, kun lopputuote valmistuu. Samoista ainesosista voidaan valmistaa useita tuotteita eri eräkoossa, useita kerralla tai eri saannoilla. Voit luoda tarvitsemasi määrän reseptiversioita.

Voit hallita useita reseptin aktiivisia versioita käyttämällä voimassaolopäivävälejä tai ”alku”-määräkenttiä. Useita aktiivisia reseptiversioita voi olla olemassa vain, jos päivämääräalueet ja "alku"-määrät eivät ole päällekkäisiä.

Toisin kuin tuoterakenteet, joissa yksi tuoterakenne liittyy usein useaan eri tuoterakenneversioon, reseptillä on yleensä vain yksi reseptiversio. Muista, että tietyn tuotteen kattavuusdimensioille ja määrälle voidaan aktivoida vain yksi reseptiversio. Reseptillä voi kuitenkin olla useita versioita muistaa syistä, ja voit valita ne manuaalisesti erätilausta luodessasi.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Hyväksy ja aktivoi reseptejä ja reseptiversioita
Reseptit ja reseptiversiot on hyväksyttävä ennen niiden käyttöä suunnittelussa ja tuotannossa. Reseptit aktivoidaan yleensä ennen käyttöä. Tuotannon aikana voit kuitenkin valita hyväksytyn reseptiversion, jota ei ole aktivoitu.

Reseptin tai reseptiversion voi suojata määrittämällä **Estä muokkaus** ja **Estä hyväksynnän poisto** -parametrit **Tuotannonhallinnan parametrit** -sivulla.

Jos valitset **Estä muokkaus** -vaihtoehdon ja resepti on hyväksytty, reseptirivien kenttiä ei voi poistaa tai muokata. Jos kuitenkin poistat reseptin hyväksynnän, voit poistaa ja muokata reseptirivejä. Voit myös luoda uusia reseptejä ja reseptiversioita.

Jos valitset **Estä hyväksynnän poisto** -vaihtoehdon, et voi poistaa hyväksytyn reseptin tai reseptiversion hyväksyntää. Voit kuitenkin luoda uusia reseptejä ja reseptiversioita, ja voit poistaa reseptiversion aktivoinnin.

Voit lisätä hallinnan tasoja käyttämällä sähköisen allekirjoituksen toimintoa. Kun käyttäjä on määritetty siten, että sähköinen allekirjoitus tarvitaan reseptin hyväksymisen yhteydessä, **Allekirjoitus**-sivu tulee näkyviin, kun kaava on aktivoitu. Käyttäjällä on oltava oikeus sähköiseen allekirjoitukseen ja sertifikaatti on tarkistettava onnistuneesti ennen muutoksen vahvistamista. Jos allekirjoitusta ei voida todentaa, hyväksyntä tai hyväksynnän poisto estetään ja muutos, joka käynnisti hyväksynnän tai sen poiston palautetaan alkuperäiseen tilaansa.

## <a name="use-the-scalable-feature"></a>Skaalaustoiminnon käyttö
Skaalattava ominaisuus on käytettävissä vain, jos kaikki reseptin nimikekomponenttien tilaksi on asetettu **Muuttuva kulutus**. Toiminto ei ole käytettävissä, jos nimikkeen komponenttien tilaksi on asetettu **Kiinteä kulutus** tai **Vaihekulutus**. Kun Skaalautuvuus-toiminto on käytössä, kaikki reseptin ainesosaan tehtävät muutokset muuttavat myös muiden valittujen ainesosien määrää. Reseptin kokoa muutetaan myös. Vastaavasti, jos reseptin kokoa muutetaan, kaikkien skaalattavien ainesosien määrä muutetaan. Tämä toiminto on tarkoitettu erityisesti reseptin luomista ja ylläpitoa varten. Se ei ilmaise, skaalataanko ainesosan määrää ylös- vai alaspäin erätilauksessa.

## <a name="use-step-consumption"></a>Vaihekulutuksen käyttö
Vaihekulutus poistaa tarpeen syöttää ainesosan määrä **Reseptirivi**-välilehdellä. Sen sijaan vaihekulutus määritetään siten, että sillä on **Sarjasta**-arvo ja **Määrä**-arvo. Erätilauksen määrän perusteella valitaan sen sarjakohtaisen vaihekulutuksen tiedot, joka vastaa kyseistä määrää. Vaihekulutuksen käyttö on hyödyllistä, kun kulutus ei ole eräkoon kannalta lineaarista, sillä se nostaa vaatimusta vain, kun tietty määräraja ylittyy. Toiminnon voi ottaa käyttöön uudessa reseptissä vaihtamalla **Kulutuksen laskenta** -ryhmässä reseptin ainesosa-asetuksen arvosta **Vakio** arvoon **Vaihe**. Voit määrittää tämän kulutusmenetelmään **Reseptirivi**-sivun **Asetukset**-välilehdellä.
