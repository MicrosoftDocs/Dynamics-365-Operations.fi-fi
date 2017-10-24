---
title: "Työvoiman hallinnan yleiskatsaus"
description: "Tässä aiheessa kuvataan, miten käytät Työvoiman hallinta (WFM) -palvelua yhdessä tuttujen myyntipistesovellusten, Modern POS ja Cloud POS -sovellusten kanssa, jotta myymäläesimiehet voivat hallita työvoimaansa helpommin."
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>Työvoiman hallinnan yleiskatsaus

[!include[banner](includes/banner.md)]
    
Työvoiman hallinta (WFM) -palvelua käyttää tuttuja myyntipistesovelluksia, eli Modern POS ja Cloud POS, jotta myymäläesimiehet voivat hallita työvoimaansa helpommin. WFM-palvelu lataa tarvittavat paketit myyntipisteelle laajennuskehyksen avulla. Paketit ladataan, kun myyntipiste suljetaan ja avataan uudelleen. Myyntipistesovellus on siis käynnistettävä uudelleen aina, kun Microsoft julkaisee uusia WFM-ominaisuuksia.

Tämän palvelun avulla myymäläesimiehet voivat luoda ja julkaista myymälänsä viikoittaiset työvuorot helposti. Myymälän työntekijät voivat sitten tarkastaa omat ja kollegoidensa työvuorot helposti. Näin he saavat tietää, kenen kanssa he työskentelevät kullakin työvuorolla. Myymälän työn tekijät voivat myös luoda poissaolo- tai vuoronvaihtopyyntöjä ja vuorotarjouksia. Kaikki pyynnöt käynnistävät määritetyn työnkulun.

Työvuoron aikana myymälän työntekijät voivat hyödyntää myyntipistesovelluksiin sisäänrakennettua kellokorttitoimintoa. Tiedot lähetetään pääkonttoriin palkanlaskennan käsittelyä varten. Kellokorttitoiminto on myyntipistesovelluksen vanhempi ominaisuus. Lisätietoja määrityksestä ja tuetuista skenaarioista on kohdassa [Saapumis- ja poistumismerkinnät](retail-time-attendance.md).

## <a name="supported-scenarios"></a>Tuetut skenaariot
Tässä osassa on lisätietoja tuetuista skenaarioita.

- **Aikataulujen luominen ja julkaisu** – WFM selvittää, onko työntekijällä myymäläesimiehen käyttöoikeus pääkonttorissa määritettyjen myyntipisteen käyttöoikeuksien perusteella. Vain myymäläpäälliköt voivat luoda ja julkaista aikatauluja aikataulun hallintatoiminnolla. He voivat luoda aikatauluja nopeasti kopioimalla ja liittämällä yhden työntekijän työvuoroja toiselle työntekijälle. Aikatauluja voi myös luoda tuomalla aikataulun mistä tahansa edellisestä työviikosta nykyiseen.

    Jos aikataulua ei ole julkaistu, se on luonnostilassa, ja se näyttää erilaiselta julkaistuun aikatauluun nähden. Myymäläesimiehet voivat julkaista aikataulun valitsemalla minkä tahansa viikon **Julkaise** -painiketta. Kun viikon aikataulu on julkaistu, kaikki siihen tehdyt muutokset julkaistaan automaattisesti. Esimerkkejä muutoksista ovat työvuorojen tai poissaolojen lisääminen, poistaminen ja muokkaus. Myymälän työntekijät voivat tarkastella vain aikatauluja, jotka on julkaistu.
    
- **Luo ja hyväksy pyyntöjä** – myymälän työntekijöille voivat luoda kolmen tyyppisiä pyyntöjä:

    - Poissaolopyyntö
    - Vuoronvaihtopyyntö
    - Vuoronvaihtotarjous

    Nämä pyynnöt luodaan Aikataulupyynnöt-toiminnolla. Jokaista pyyntöä seuraa määritetty työnkulku, ja työntekijät näkevät pyyntöjensä tilan helposti.
    
    Poissaolopyynnöt lähetetään automaattisesti myymäläesimiehen hyväksyttäväksi. Jos myymäläesimiehiä on useita, kaikki esimiehet voivat tarkastella pyyntöjä, mutta vain yksi esimies voi hyväksyä tai hylätä sen. Poissaolotyypit määritetään vähittäismyynnin pääkonttorissa **Vähittäismyynti**-moduulin **Loma- ja poissaolotyypit** -sivulla. Kun myymäläpäällikkö hyväksyy tai hylkää pyynnön, se siirretään Aikataulupyynnöt-toiminnon **Historia**-välilehdelle.
    
    Vuoronvaihto tai vaihtotarjous lähetetään ensin työntekijälle, jolle pyyntö on osoitettu. Myymäläpäällikkö voi tarkastella pyyntöä vasta, kun kyseinen työntekijä on hyväksynyt sen. Jos työntekijä siis hylkää vuoronvaihto- tai vaihtotarjouspyynnön, se ei tule esimiehen nähtäville. Pyynnön luonut työntekijä voi myös perua pyynnön, ennen kuin esimies hyväksyy tai hylkää pyynnön.

- **Näytä myymälän aktiiviset työntekijät aikataulunäkymässä** – kun työntekijä lisätään myymälään, esimerkiksi liittämällä tämä myymälän työntekijäosoitekirjaan, työntekijä on aikataulutettavissa WFM-palvelussa. Toistuva erätyö, jonka nimi on **Käsittele työvoiman hallinnan työntekijätiedot** suoritetaan pääkonttorissa. Tämä työn valmistelee myymälä-työntekijäliitokset, jotka lähetetään Common Data Service -palveluun (CDS).

    Samaa prosessia käytetään, kun työntekijä poistetaan myymälästä. Poistettu työntekijä näytetään kuitenkin menneissä, nykyisissä ja tulevissa viikoissa, jos ko. työntekijälle on määritetty aktiivinen työvuoro tai poissaolo. Ellei näitä työvuoroja ja poissaoloja poisteta, työntekijä näkyy edelleen näillä viikoilla.

