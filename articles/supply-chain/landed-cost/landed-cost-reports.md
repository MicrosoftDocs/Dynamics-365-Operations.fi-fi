---
title: Aiheutunut kustannus -raportit
description: Tässä aiheessa kuvataan, miten Aiheutunut kustannus -moduulissa käytettävissä olevia erilaisia raportteja löytyy ja käytetään.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: cb0ea44c0924fc5d2c295a9285701d1f678c3473
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571734"
---
# <a name="landed-cost-reports"></a>Aiheutunut kustannus -raportit

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>Avoimet laskut

Avoimien laskujen raportti sisältää luettelon kaikista avoimista laskuista eri kustannustasoilla, jotka liittyvät jokaiseen merikuljetukseen. Sen avulla voit täsmäyttää merikuljetuksen ja merikuljetuksen kustannukset kirjanpidon tapahtumien kanssa säännöllisin väliajoin. Kun yleiskustannus on laskutettu, se poistetaan raportista.

Voit luoda avoimien laskujen raportin seuraavasti.

1. Valitse **Aiheutunut kustannus \> Raportit \> Seuranta \> Avoimet laskut**.
1. Määritä päivämäärä **Avoimet laskut** -valintaikkunassa **Päivämääränä**-kentässä. Kaikki kyseisenä päivänä tai sitä aiemmin avoimena olevat laskut sisällytetään tuotoksen laskuun.
1. Valitse **Näytä**-kohdassa jokin seuraavista vaihtoehdoista:

    - **Kustannusta ei laskutettu** – Sisällytä laskutettujen lähetysten kustannukset, joissa on arvioitu kustannusarvo mutta ei toteutuneita kustannuksia.
    - **Varastoa ei laskutettu** – Sisällytä laskutetut kustannukset, joista ei ole vielä vastaanotettu ostotilausta.
    - **Kaikki ei-laskutetut** – Sisällytä tulokset sekä **Kustannusta ei laskutettu** -vaihtoehdosta että **Varastoa ei laskutettu** -vaihtoehdosta.

1. Määritä **Sisällytä uudet kustannukset** -asetuksen arvoksi *Kyllä*, jos haluat sisällyttää kustannukset, joilla ei ole vielä toteutunutta kustannusta ja jolle ei ole vielä vastaanotettu varastoa. Jos määrität arvoksi *Ei*, raportti sisältää vain laskutetut kustannukset.
1. Ota **Näytä**-osassa käyttöön kaikki raporttiin sisällytettävät tiedot.
1. Kuten muitakin raportteja varten Microsoft Dynamics 365 Supply Chain Managementissa valitse raportin tulostusmuoto **Kohde**-pikavälilehden avulla.
1. Kuten muitakin Supply Chain Managementin raportteja varten voit rajoittaa raporttiin sisällytettäviä tyyppejä lisää käyttämällä **Sisällytettävät tietueet** pikavälilehteä.
1. Luo raportti valitsemalla **OK**.

## <a name="activityprovider-analysis-reports"></a>Tehtävän/palveluntarjoajan analyysiraportit

Tehtävän/palveluntarjoajan analyysiraporttien avulla voit tarkistaa kunkin palveluntarjoajan aika-arviosi tarkkuuden.

Voit luoda tehtävän/palveluntarjoajan analyysiraportin seuraavasti.

1. Luotavan raportin tyypistä riippuen noudata seuraavia vaiheita:

    - Valitse **Aiheutunut kustannus \> Raportit \> Tehtävän/palveluntarjoajan analyysi tehtävän mukaan**. Tällöin aika-arviot ryhmitellään tehtävän mukaan.
    - Valitse **Aiheutunut kustannus \> Raportit \> Tehtävän/palveluntarjoajan analyysi palveluntarjoajan mukaan**. Tällöin aika-arviot ryhmitellään palveluntarjoajan mukaan.

    Näkyviin tulee joko **Tehtävän/palveluntarjoajan analyysi tehtävän mukaan**- tai **Tehtävän/palveluntarjoajan analyysi palveluntarjoajan mukaan** -valintaikkuna. Samat vaihtoehdot ovat käytettävissä molemmissa valintaikkunoissa.

1. Kuten muitakin raportteja varten Supply Chain Managementissa valitse raportin tulostusmuoto **Kohde**-pikavälilehden avulla.
1. Kuten muitakin Supply Chain Managementin raportteja varten voit rajoittaa raporttiin sisällytettäviä tyyppejä lisää käyttämällä **Sisällytettävät tietueet** pikavälilehteä.
1. Luo raportti valitsemalla **OK**.

## <a name="voyage-costing-reports"></a>Merikuljetuksen kustannuslaskentaraportit

Sen mukaan, mitä vaihtoehtoja valitset raportin muodostuksissa, voit näyttää merikuljetuksen kustannuslaskentaraporteissa nimikkeiden kustannukset ja tuontikustannukset pakkausta, kuljetuskonttia tai merikuljetusta kohden. Jokaisessa merikuljetuksen kustannuslaskentaraportissa voit vertailla arvioituja merikuljetuksen arvioituja ja todellisia kustannuksia, ja ne voidaan jakaa useiden tunnistustekijöiden mukaan.

Voit luoda merikuljetuksen kustannuslaskentaraportin seuraavasti.

1. Luotavan raportin tyypistä riippuen noudata seuraavia vaiheita:

    - Valitse **Aiheutunut kustannus \> Raportit \> Kustannuslaskenta \> Merikuljetuksen kustannuslaskenta yksittäisen kustannuksen mukaan**. Tässä tapauksessa yksittäinen kustannusvaihtoehto näyttää tuontikustannukset kustannusalueittain kustannustyyppikoodia kohti.
    - Valitse **Aiheutunut kustannus \> Raportit \> Kustannuslaskenta \> Merikuljetuksen kustannuslaskenta raportointiluokan mukaan**. Tässä tapauksessa tuontikustannukset jaetaan eri raportointiluokkiin. Kustannustyypit on ryhmitelty raportointiluokkien mukaan.

    Näkyviin tulee joko **Merikuljetuksen kustannuslaskenta yksittäisen kustannuksen mukaan**- tai **Merikuljetuksen kustannuslaskenta raportointiluokan mukaan** -valintaikkuna. Nämä valintaikkunat ovat samankaltaisia. Mahdolliset erot on kerrottu menetelmän loppuosassa.

1. Jos avasit **Merikuljetuksen kustannuslaskenta raportointiluokan mukaan** -valintaikkunan, valitse **Kustannus**-kentästä jokin seuraavista arvoista:

    - **Kustannusarvo** – Arvo lasketaan joko automaattisia kustannuksia käyttäen tai luodaan manuaalisesti kustannusalueella.
    - **Arvioitu** – Kun tavarat on vastaanotettu, arvioidut kustannukset määritetään.
    - **Todellinen** – Kun tilaus on laskutettu, todelliset kustannukset määritetään laskun kustannuksiksi.
    - **Paras** – Järjestelmä käyttää jotakin sen mukaan, mik' näistä kolmesta edellisestä vaihtoehdosta on tarkempi. (On suositeltavaa valita tämä asetus.)

1. Määritä **Nimikekohtainen**-asetuksen arvoksi *Kyllä*, jos haluat näyttää kunkin nimikkeen kustannukset. Määritä sen arvoksi *Ei*, jos haluat näyttää kustannukset merikuljetusta kohden.
1. Valitse **Näytä**-osassa luokat, jonka mukaan kustannus jaetaan.
1. Valitse **Dimensiot**-osassa raporttiin sisällytettävät dimensiot.
1. Kuten muitakin raportteja varten Supply Chain Managementissa valitse raportin tulostusmuoto **Kohde**-pikavälilehden avulla.
1. Kuten muitakin Supply Chain Managementin raportteja varten voit rajoittaa raporttiin sisällytettäviä tyyppejä lisää käyttämällä **Sisällytettävät tietueet** pikavälilehteä.
1. Luo raportti valitsemalla **OK**.

## <a name="shipping-container-receipts-list"></a>Lähetyskonttien vastaanottoluettelo

Kuljetuskontin vastaanottoluettelo sisältää kaikki vastaanottamattomat määrät, jotka erääntyvät odotettuna päivämääränä tai ennen sitä. Varaston henkilökunta voi tämän raportin avulla tunnistaa kuljetuskontin odotetut tavarat. Sen avulla voidaan myös tarkistaa manuaalisesti tavarat, kun ne vastaanotetaan kuljetuskontissa.

Luo kuljetuskontin vastaanottoluettelo noudattamalla seuraavia ohjeita.

1. Valitse **Aiheutunut kustannus \> Raportit \> Seuranta \> Kuljetuskontin vastaanottoluettelo**.
1. Määritä päivämäärä **Kuljetuskontin vastaanottoluettelo** -valintaikkunan **Odotettu päivämäärä** -kentässä. Kaikki kyseisenä päivänä tai sitä aiemmin vastaanottamattomat määrät sisällytetään tuotoksen laskuun.
1. Valitse **Dimensiot**-osassa raporttiin sisällytettävät dimensiot.
1. Kuten muitakin raportteja varten Supply Chain Managementissa valitse raportin tulostusmuoto **Kohde**-pikavälilehden avulla.
1. Kuten muitakin Supply Chain Managementin raportteja varten voit rajoittaa raporttiin sisällytettäviä tyyppejä lisää käyttämällä **Sisällytettävät tietueet** pikavälilehteä.
1. Luo raportti valitsemalla **OK**.

## <a name="expected-delivery-report"></a>Odotettu toimitus -raportti

Odotettu toimitus -raportti sisältää perustiedot merikuljetuksesta, kuljetuskontista, pakkauksesta, nimikkeistä ja odotetusta toimituspäivästä.

Voit luoda odotetun toimitusraportin seuraavasti.

1. Valitse **Aiheutunut kustannus \> Raportit \> Seuranta \> Odotettu toimitus**.
1. Valitse **Odotettu toimitus** -valintaikkunan **Odotettu päivämäärä** -kentässä päivämäärä, jolloin tavaroiden toimitusta lopulliseen kohdevarastoon odotetaan. Kaikki merikuljetuksen rivit, joiden odotettu päivämäärä on kyseisenä päivänä tai sitä ennen ja joita ei ole vielä vastaanotettu, sisällytetään tuotokseen.
1. Valinnainen: Valitse **Toimittajatili**-kentästä toimittajatili, jos haluat sisällyttää vain tietyn toimittajan toimitukset.
1. Valitse **Dimensiot**-osassa raporttiin sisällytettävät dimensiot.
1. Kuten muitakin raportteja varten Supply Chain Managementissa valitse raportin tulostusmuoto **Kohde**-pikavälilehden avulla.
1. Kuten muitakin Supply Chain Managementin raportteja varten voit rajoittaa raporttiin sisällytettäviä tyyppejä lisää käyttämällä **Sisällytettävät tietueet** pikavälilehteä.
1. Luo raportti valitsemalla **OK**.
