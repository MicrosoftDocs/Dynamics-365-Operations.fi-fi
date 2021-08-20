---
title: Kalenterit ja pääsuunnittelu
description: Tässä ohjeaiheessa on yleiskatsaus toimitusketjujen kalentereista ja niiden vaikutuksesta pääsuunnitteluun.
author: t-benebo
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a2b6f1c3d98ca8265dea83bde4bc5e7d677da3d88533d39fe06a49a61cb1b9ea
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771416"
---
# <a name="calendars-and-master-planning"></a>Kalenterit ja pääsuunnittelu

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on yleiskatsaus toimitusketjujen kalentereista ja niiden vaikutuksesta pääsuunnitteluun.  Pääsuunnittelumoduulissa käytettävät erilaiset kalenterit esitellään. Lisäksi käsitellään niiden vaikutus suunniteltujen tilausten lähetys- ja vastaanottopäiviin. Lopuksi annetaan kalenterien määritystä, käyttöä ja päivitystä koskevia suosituksia.

## <a name="definition-of-a-calendar"></a>Kalenterin määritelmä

Voit määrittää organisaatiossa käytettävän kalenterin sivulla, jonka voit avata valitsemalla **Organisaation hallinto > Asetukset > Kalenterit > Kalenterit**. 

Kalenterin päivämäärämerkintä on joko **avoin**, **suljettu** tai **peruskalenteri**. Se määritetään **Työajat**-sivun **Ohjausobjekti**-sarakkeessa. Päivämääräkohtaisesti: 
- **Avoin** – Ilmaisee, että työ tehdään valittuna päivänä. Kalenteri päivitetään työaikamallin mukaisesti.
- **Suljettu** – Ilmaisee, että työtä ei tehdä päivän aikana. 
- **Peruskalenteri** – Ilmaisee, että tietty päivä perii työajat ja avoin/suljettu-merkinnän peruskalenterista. Niinpä kun peruskalenteri päivitetään, valittu kalenteri perii työajat siitä. 

**Suljettu noudolta** -valintaruutu määritetään automaattisesti suljetuille päivämäärille. Voit valita **Suljettu noudolta** -asetuksen manuaalisesti avoimille päivämäärille. Tämä ilmaisee, että suoritetaan kyseisenä päivämääränä mutta lähetys ei tehdä. 

## <a name="calendars-that-affect-master-planning"></a>Pääsuunnitteluun vaikuttavat kalenterit

### <a name="calendar-for-a-coverage-group"></a>Kattavuusryhmän kalenteri
Kattavuusryhmä ilmaisee tiettyyn kattavuusryhmään kuuluvien nimikkeiden täyttämiseen käytetyn yleisen parametrijoukon. 

Lisää kattavuusryhmän kalenteri valitsemalla **Pääsuunnittelu > Asetukset > Kattavuus > Kattavuusryhmät**. Etsi kattavuusryhmä, johon haluat määrittää kalenterin, ja valitse se **Kalenteri**-kentässä.

Kattavuusryhmä voidaan määrittää eri sivuilla: 
    - Nimikkeen **Vapautetun tuotteen tiedot** -sivu. Jos haluat nähdä nimikkeen kattavuusryhmän valitse **Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet** ja siirry sitten **Vapautettujen tuotteiden tiedot** -sivulle valitsemalla nimike. Nimikkeen kattavuusryhmä näkyy **Suunnitelma**-pikavälilehdessä.
    - **Nimikkeen kattavuus** -sivulla. Siirry nimikkeen kattavuussivulle valitsemalla vapautettujen tuotteiden tietosivulla **Nimikkeen kattavuus**. Yhteenvetovälilehdessä on erilaisia täydennysparametreja, jotka määräytyvät toimipaikan, varaston ja tuotedimensioiden mukaan. Kunkin nimikkeen kattavuusryhmä peritään **Vapautetun tuotteen tiedot** -sivun kattavuusryhmästä. Se voidaan ohittaa valitsemalla **Yleiset**-välilehdessä **Käytä erityisasetuksia** tai **Korvaa ryhmän asetukset**.
    - **Pääsuunnittelun parametrit** -sivulla. Jos nimikkeelle ei ole määritetty kattavuusryhmää edellisillä sivuilla, pääsuunnittelu käyttää pääsuunnittelun parametreissa määritettyä yleistä kattavuusryhmää. Se määritetään valitsemalla **Pääsuunnittelu > Asetukset > Pääsuunnittelun parametrit** **Yleinen kattavuusryhmä** -kentässä. 

### <a name="calendar-for-a-vendor"></a>Toimittajan kalenteri
Voit ilmoittaa toimittajan työpäivät määrittämällä toimittajalla ostokalenterin toimittajan **Oletusostotilaukset**-sivulla. 

Toimittajan kalenteria varten on luotava kalenteri valitsemalla **Organisaation hallinto > Kalenterit > Kalenterit**. Kun kalenteri on luotu, se on määritettävä toimittajalle. Valitse ensin **Ostoreskontra > Toimittajat > Kaikkien toimittajat** ja valitse sitten toimittaja, jolle haluat määrittää kalenterin. Määritä seuraavaksi **Oletusostotilaukset**-pikavälilehden toimittajan sinulla uusi ostokalenteri avattavan valikon avulla. 

Toimittajan kalenteri ilmaisee päivät, jolloin ostotilauksen teko hyväksytään, ja päivämäärät, jolloin tilaukset voidaan toimittaa yrityksellesi. Niinpä sellaisen toimittajan ostotilausten tilauspäivämäärät, joilla on ostokalenteri, ovat kalenterissa avoimeksi määritettyjä päivämääriä. Myös näiden tilausten toimituspäivämäärät ovat avoimia päiviä, mikä puolestaan vaikuttaa ostetun nimikkeen läpimenoaikaan. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>Ostetun nimikkeen läpimenoajan määrittäminen

Voit määrittää nimikkeen oston läpimenoajan (ja otetaanko vain työpäivät huomioon) siirtymällä tuotteen oletustilausasetuksiin valitsemalla ensin **Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet** ja sitten **Tilauksen oletusasetukset**. 

> [!Note]
> Oston läpimenoajan kohdalla olevia **Työpäivät** tarkoittaa toimittajan työpäiviä. Esimerkki: jos kalenteri koskee vain tiistaitoimituksia, läpimenoaika on 10 päivää ja työpäivien valintaruutu on valittu, se tarkoittaa, että nimikkeen toimittamiseen kuluu 10 viikkoa (10 tiistaita).
Tämän vuoksi työpäivien valintaa ostotilauksen läpimenoajalle ei yleensä suositella.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Läpimenoaikojen määrittäminen kauppasopimussivulta

Pääsuunnittelu voidaan määrittää sisältämään kaikki toimittajien kauppasopimukset. Kauppasopimukset ovat kiinteitä hintoja tai alennussopimuksia, jotka on määritetty vähintään yhdelle asiakkaalle tai toimittajalle yksittäisten tuotteiden tai useiden tuotteiden myyntiä tai ostamista varten. Valitse ensin **Pääsuunnittelu > Asetukset > Pääsuunnittelun parametrit** ja valitse sitten **Suunnitellut tilaukset** -välilehdessä **Etsi kauppasopimukset**, jos haluat sisällyttää kauppasopimukset suunnitteluun. Pääsuunnittelu voi valita toimittajan, jolla on joko **Minimiläpimenoaika** tai **Alhaisin yksikköhinta**.

### <a name="calendar-for-a-warehouse"></a>Varaston kalenteri
Voit määrittää kalenterin varastoon ilmaisemaan avoimet vastaanotto- ja lähetyspäivämäärät. Jos varastolle ei ole määritetty kalenteria, sen oletetaan olevan avoinna joka päivä. 

> [!Note]
> Kalenterin määrittämisellä kuljetusvarastolle ei ole mitään vaikutusta. Kuljetusvarastoilla tuetaan siirtotilauksia. Tilauksille soveltuvat lähetys- tai vastaanottopäivämäärät määritetään lähtö- ja kohdevarastojen avoimien päivämäärien ja toimituskalenterin tilan mukaan.

#### <a name="closed-for-pickup-policy"></a>Suljettu noudolta -käytäntö
Jos haluat ilmaista, että varasto on avoin vastaanotolle mutta nouto ei ole mahdollista, voit käyttää varastokalenterissa **Suljettu noudolta -käytäntöä**. Tämä koskee myös asiakkaan noutoja. 

### <a name="transport-calendar"></a>Kuljetuskalenteri 
Jos haluat ilmaista siirtotilausten **Varastosta**-lähetykseen käytettävissä olevat päivämäärät, voit määrittää **kuljetuskalenterin**. Kuljetuskalenterin voi määrittää kahdella tavalla: toimitustavan mukaan tai toimitustavan mukaan ja varastosta. Kuljetuskalenteri määritetään valitsemalla **Myynti ja markkinointi > Asetukset > Jakelu > Toimitustavat**. Valitse toimitustapa ja napsauta sitten **Kuljetuskalenteri**-painiketta.

Kullekin varastolle ja toimitustavalle voidaan luoda rivi, johon kalenteri lisätään **Kuljetuskalenteri**-sarakkeessa. Se määrittää kuljetuskalenterin, jota käytetään, kun tavarat lähetetään varastosta annetulla toimitustavalla. Jos kuljetuskalenteria halutaan käyttää kaikkiin tiettyä toimitustapaa käyttäviin lähetyksiin, rivi voidaan luoda varastoa määrittämättä.  Se koskee kaikkia annettua toimitustapaa käyttäviä lähetyksiä varastosta riippumatta. 

Jos mitään kuljetuskalenteria ei ole määritetty, kaikkien päivien oletetaan olevan avoimia kuljetukselle.

### <a name="calendar-for-a-customer"></a>Asiakkaan kalenteri
Voit ilmaista päivämäärät, jolloin asiakas voi vastaanottaa toimituksia, määrittämällä asiakkaalle vastaanottokalenterin. Jos asiakkaalle ei ole määritetty mitään kalenteria, asiakkaan oletetaan voivan vastaanottaa tilauksia kaikkina päivinä. Se vaikuttaa myyntitilausrivien vastaanottopäivään. Jos valitset myyntitilausriveillä päivämäärän, joka ei ole avoin asiakkaan kalenterissa, järjestelmä ilmaisee, että vastaanottopäivämäärä ei kelpaa. 

Huomaa, että kullekin asiakkaalle voidaan sisällyttää vain yksi kalenteri. Jos asiakkaan kullekin osoitteelle on sisällytettävä kalenteri, voit luoda kullekin osoitteelle yhden asiakkaan ja määrittää sitten sille kalenterin. 

Asiakkaan kalenteri ja toimituspäivän valvontamenetelmä vaikuttavat myyntitilausrivin pyydettyyn vastaanottopäivään. Lisätietoja aikaisimman toimituspäivän laskemistavasta [luvatuissa tilauksissa.](/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations).

### <a name="shipping-calendar-for-a-legal-entity"></a>Yrityksen lähetyskalenteri
Voit ilmaista päivämäärät, jolloin yritys voi lähettää tavaroita, määrittämällä lähetyskalenterin valitsemalla **Organisaation hallinto > Organisaatiot > Yritykset**. Valitse yritys ja lisää kalenteri **Lähetyskalenteri**-kentän **Ulkomaankauppa ja logistiikka** -välilehdessä. Lähetyskalenteri toimii yrityksen kaikkien varastokalenterien oletusarvojen lähteenä. 

## <a name="how-calendars-affect-dates-in-planning"></a>Kalenterien vaikutus suunnittelun päivämääriin

### <a name="order-date-of-a-planned-purchase-order"></a>Suunnitellun ostotilauksen tilauspäivämäärä 
Suunnitellun ostotilauksen tilauspäivämäärä ilmaisee päivämäärän, jolloin tilaus tehtiin. Se on avoin päivämäärä sekä toimittajan että kattavuusryhmän kalenterissa. Toimittajat voivat joskus tarvita muutaman päivän ostotilauksen vastaanottamisen jälkeen, ennen kuin ne voivat lähettää tavarat. Nämä päivämäärät ilmaistaan toimittajan marginaalipäivinä. Jos ostettu nimike on kuitenkin määritetty kattavuusryhmälle, jolla on marginaalipäiviä, nämä marginaalipäivät ohittavat toimittajan marginaalipäivät.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Suunnitellun ostotilauksen toimituspäivämäärä
Oston vastaanottopäivämäärä ilmaisee päivämäärän, jolloin vastaanotot tavarat. Se on kalenterin avoin päivämäärä. Seuraavat kalenterit otetaan huomioon, kun ilmaistaan, minä päivinä ostotilaukset voidaan vastaanottaa. Kalenterit on järjestetty prioriteetiltaan suurimmasta pienimpään. 
1. Toimittajan kalenteri
1. Kattavuusryhmän kalenteri
1. Vastaanottovaraston varaston kalenteri

Huomaa, että kattavuusryhmän kalenteri voidaan määrittää eri sivuilla, joiden prioriteettijärjestys on seuraava:
1. Nimikkeen kattavuusryhmä **Nimikkeen kattavuus** -sivulla
1. Nimikkeen kattavuusryhmä **Julkaistujen tuotteiden tiedot** -sivu
1. Nimikkeen oletuskattavuusryhmä **Pääsuunnittelun parametrit**

### <a name="shipping-date-of-a-planned-transfer-order"></a>Suunnitellun ostotilauksen lähetyspäivämäärä
Kun kahden varaston välille luodaan siirtotilaus, lähetys- ja vastaanottopäivämäärä sisältyvät siirtotilauksen otsikkoon, jossa on myös lähettävä ja vastaanottava varasto. Näiden kahden päivämäärän välinen ero on odotettu kuljetusaika (päivinä) varastojen välillä.

Suunnitellun siirtotilauksen lähetyspäivämäärä ilmaisee päivämäärän, jolloin tavarat lähetetään varastosta. Käytettävissä olevan lähetyspäivämäärän määrittämisessä käytetyt kalenterit prioriteetin mukaisessa järjestyksessä: 
1. Lähettävän varaston varastokalenterin
1. Kattavuusryhmän kalenteri (katso edellä tämän kalenterin varmistustilaus) Jos varastokalenteri on määritetty, lähetyspäivämäärä on avoin päivämäärä kalenterissa. Jos varastokalenteria ei ole määritetty, käytössä on kattavuusryhmän kalenteri. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Suunnitellun ostotilauksen vastaanottopäivämäärä
Siirtotilauksen vastaanottopäivämäärä ilmaisee päivämäärän, jolloin tavarat vastaanotetaan varastoon.

Vastaanottopäivämäärän määrittämisessä käytetyt kalenterit prioriteetin mukaisessa järjestyksessä: 
1. Kattavuusryhmän kalenteri 
1. Vastaanottavan varaston varastokalenteri Jos kattavuuskalenteri on määritetty, vastaanottopäivämäärä on avoin päivämäärä kalenterissa. Jos kattavuusryhmän kalenteria ei ole määritetty, käytössä on varastokalenteri. 

Kun suunnitellun siirron lähetys- ja vastaanottopäivämääriä etsitään, huomioon otetaan myös käyttäjän lähettämiselle ja vastaanottamiselle määrittämät marginaalit. 

## <a name="using-calendars-in-master-planning"></a>Kalenterien käyttäminen pääsuunnittelussa

### <a name="assignment-of-scm-calendars"></a>SCM-kalenterien määritys
On tärkeää määrittää kalenterit siten, että ne tunnistavat yrityksen työpäivät. Paras tapa tehdä tämä on määrittää kalenteri kullekin elementille, jolla on erilaiset työpäivät. Toisin sanoen kyse on kaikista yrityksiin liittyvistä ulkoisista kalentereista (asiakas, toimittaja) ja sisäisistä kalentereista (varasto, kattavuusryhmä ja toimitustapa).

### <a name="recommendation-on-warehouse-calendars"></a>Varaston kalenterisuositus
On suositeltavaa käyttää yhtä varastokohtaista kalenteria, joka sisältää vain varastoon vaikuttavat muutokset. Kahdella tai useammalla varastolla voi esimerkiksi olla samat työpäivät mutta erilainen noutokäytäntö. Tässä tapauksessa kalenteri kullekin varastolle noutokäytäntöineen on paras toteutus, sillä silloin järjestelmä sisällyttää parhaat päivämäärät suunnitellulle ostolle, siirrolle ja tuotantotilauksille. Jos varaston kalentereita ei ole määritetty, yrityksen kalenteria voidaan käyttää varaston kalenterin oletusarvojen lähteenä. 

### <a name="recommendation-of-coverage-group-calendars"></a>Kattavuusryhmän kalenterisuositus
Kattavuusryhmän kalenterissa on tärkeää ottaa huomioon, että sen toiminta ohittaa pääsuunnittelun vastaanottopäivämäärät. Tämän vuoksi sen käytön kanssa on oltava huolellinen. Se on kuitenkin kätevä tapauksissa, joissa täydennys on tehtävä tiettynä viikonpäivinä. 

### <a name="updating-scm-related-calendars"></a>Liittyvien SCM-kalenterien näyttäminen
Vaikka on tärkeää, että kaikki soveltuvat kalenterit määritetään asianmukaisesti (toimittaja, asiakas, varasto, toimitustapa tai kattavuusryhmä), niiden päivittäminen näyttämään muutokset on tärkeää. Järjestelmä määrittää tuotannon, siirron, oston ja myyntitilauksen päivämäärät määritettyjen kalenterien yhdistelmän mukaan. On parhaan käytännön mukaista selventää, kuka vastaa kalenterien määrittämisestä ja päivittämisestä kyseisillä alueilla. Mikäli työpäivinä tapahtuu käyttökatkos tai silloin epätavallisia muutoksia, on erittäin tärkeää, että kalenterit päivitetään vastaavasti. Kaikki kalenterista riippuvat tapahtumat, kuten pääsuunnittelu ja tuotannon aikataulutus, on suoritettava uudelleen, kun kalenterit päivitetään. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]