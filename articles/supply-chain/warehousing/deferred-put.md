---
title: Varastotyön lykätty käsittely
description: Tässä artikkelissa käsitellään toimintoja, joiden avulla varastotyön lykätty käsittely on mahdollista Dynamics 365 Supply Chain Managementissa.
author: Mirzaab
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f4eeea0805c2cecedbd6b42926191ab02022df9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899292"
---
# <a name="deferred-processing-of-warehouse-work"></a>Varastotyön lykätty käsittely

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan toimintoja, joiden avulla varastotyön lykätty käsittely on mahdollista Dynamics 365 Supply Chain Managementissa.

Lykätyn käsittely toiminnon avulla varastotyöntekijät jatkavat työskentelyä, kun hyllytystoimintoa käsitellään taustalla. Lykätty käsittely on kätevää, kun useita työrivejä on käsiteltävä ja työntekijä voi antaa työn käsittelyn toimia asynkronisesti. Se on hyödyllinen myös silloin, kun palvelimella voi olla ad-hoc-tai suunnittelemattomia lisäyksiä käsittelyaikaan, ja lisääntynyt käsittelyaika saattaa vaikuttaa käyttäjän tuottavuuteen.

Taustakäsittely saavutetaan käyttämällä SysOperation-kehystä. Lisätietoja saat ohjeaiheesta [SysOperation-kehyksen yleiskatsaus](/dynamicsax-2012/developer/sysoperation-framework-overview).

## <a name="configuring-the-work-processing-policies"></a>Työn käsittelykäytäntöjen konfiguroiminen

Jos haluat käyttää lykättyä käsittelyä, sinun on konfiguroitava ja käytettävä työn käsittelykäytäntöä.

Käytännöt määritetään **Työn käsittelykäytännöt** -sivulla. Seuraavassa taulukossa näkyvät tämän sivun kentät.

| Kenttä                           | Kuvaus |
|---------------------------------|-------------|
| Työn prosessoinnin käytännön nimi     | Työn käsittelykäytännön nimi. |
| Työtilaustyyppi                 | Työtilaustyyppi, johon käytäntöä sovelletaan. |
| Toiminto                       | Käytännön avulla käsiteltävä työvaihe. |
| Työn käsittelymetodi          | Menetelmä, jota käytetään työrivin käsittelyyn. Jos menetelmän arvoksi on määritetty **Välitön**, käyttäytyminen muistuttaa toimintaa, jolloin rivin käsittelyyn ei käytetä työn käsittelykäytäntöjä. Jos menetelmän arvoksi on määritetty **Lykätty**, käytetään eräkehystä käyttävää lykättyä käsittelyä. |
| Lykätty käsittelykynnys   | Arvo **0** (nolla) tarkoittaa, että raja-arvoa ei ole. Tässä tapauksessa käytetään lykättyä käsittelyä, jos sitä voidaan käyttää. Jos tietyn raja-arvon laskenta on kynnysarvon alapuolella, käytetään Välitön-menetelmää. Muussa tapauksessa käytetään Lykätty-menetelmää, jos sitä voidaan käyttää. Myyntiin ja siirtoon liittyvän työn osalta kynnys lasketaan työhön liittyvien lähdekuormitusrivien määrän mukaan. Täydennystyötä varten raja-arvo lasketaan työrivien määräksi, joita työ täydentää. Jos määrität raja-arvoksi esimerkiksi **5** myynnille, pienemmät työt, joissa on vähemmän kuin viisi alkuperäistä lähdekuormitusriviä, eivät käytä lykättyä käsittelyä, mutta suuremmissa töissä sitä käytetään. Kynnys vaikuttaa vain, jos työn käsittelymenetelmä on **Lykätty**. |
| Lykätty käsittelyn eräryhmä |Eräryhmä, jota käytetään käsittelyyn. |

Seuraavia hyllytyksen käsittelytehtävien työtilaustyyppejä tuetaan: myyntitilaus, siirtotilauksen varasto-otto ja täydennys.

## <a name="assigning-the-work-creation-policy"></a>Työn luontikäytännön määrittäminen

Työn luontikäytäntö voidaan määrittää varastonhallinnan parametreissa. Se voidaan määrittää myös yksilöllisten varastojen tasolla. Jos käytäntö on liitetty varastoon, sitä käytetään vain kyseiselle varastolle luodulle työlle. Jos mitään käytäntöä ei määritetä varastotasolla, käytetään varaston hallintaparametrien käytäntöä.

## <a name="viewing-the-deferred-put-processing-tasks"></a>Lykättyjen hyllytyskäsittelytehtävien tarkasteleminen

Voit tarkastella lykättyjä hyllytyksen tehtäviä **Lykätyt hyllytyksen käsittelytehtävät** -sivulla.

Oletusarvon mukaan **Valmis**-tehtävät näytetään.

| Kenttä            | Kuvaus |
|------------------|-------------|
| Tila           | Tehtävän tila. |
| Erätyön tila | Liittyvän erätyön tila. Jos erätyö on käsitelty, erähistoria sisältää eräajon lokin ja tiedot. |

Seuraavassa on selitetty mahdolliset tilat:

- **Odottaa** – liittyvä erätyö odottaa käsittelyä eräpalvelimessa.
- **Epäonnistui** – käsittely epäonnistui. Tehtävä voidaan käsitellä uudelleen **Käsittele lykätty hyllytys** -toiminnon avulla tai se voidaan peruuttaa käyttämällä **Peruuta lykätty hyllytys** -toimintoa.
- **Valmis** – työ on suoritettu.

## <a name="impact-on-closed-work-dates"></a>Vaikutus suljettuihin työpäiviin

Kun käytetään lykättyä hyllytystä, suljettu käsittelypäivämääräksi määritetään lykätyn hyllytyskäsittelyn tehtävien luontipäivä ja -aika. Suljettua työpäivämäärää käytetään, koska se on paras arvio siitä, milloin hyllytystyövaihe on saatu valmiiksi.

## <a name="reprocessing-a-failed-task"></a>Epäonnistuneen tehtävän uudelleenkäsittely

Voit käsitellä epäonnistuneen tehtävän uudelleen valitsemalla sen sivulta ja valitsemalla sitten **Käsittele lykätty hyllytys**. Uudelleenkäsittely vastaa tilannetta, jossa käyttäjä viimeistelee hyllytyksen mobiililaitteessa aivan kuin se olisi määritetty välittömään käsittelyyn.

## <a name="canceling-failed-tasks"></a>Epäonnistuneiden tehtävien peruuttaminen

Vain epäonnistuneet tehtävät voidaan peruuttaa. Kun peruutat tehtävän, voit määrittää sen uudelle käyttäjälle. Vaihtoehtoisesti tehtävä säilyy edelleen määritettynä työn käsittelijälle. Peruutus vastaa tilannetta, jossa työ tuodaan takaisin mobiililaitteeseen aivan kuin viimeinen poiminta vaihe olisi juuri saatu valmiiksi ja työ täytyy hyllytellä. Käyttäjä voi kuitenkin määrittää, että työ on "erilainen", koska sillä on vain hyllytysvaihe, ja sijainti vastaa sijaintia, jonka ensimmäinen työntekijä oli määrittänyt hyllytyksen viimeiseksi varastopaikaksi.

Kun tehtävä peruutetaan, lykätyn käsittelyn eston syyn vuoksi työtä ei enää estetä. Se voidaan käsitellä uudelleen käyttämällä mobiililaitetta.

Tehtävän tietue poistetaan, kun tehtävä peruutettiin.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Mobiililaitteen valikon määrittäminen ohittamaan lykätty käsittelykäytäntö

Voit määrittää mobiililaitteen valikkovaihtoehdon niin, että lykättyä käsittelykäytäntöä ei käytetä. Työ käsitellään siten kuin se on, kun lykättyä käsittelykäytäntöä ei käytetä. Tämän toiminnon avulla valvoja voi käyttää tiettyä valikkokohdetta, jossa lykättyä hyllytystä ei käytetä. Voit määrittää sen määrittämällä **Lykätty hyllytyksen käsittelykäytäntö** -kentän arvoon **Ohita asetukset ja käsittele hyllytys synkronoidusti**. 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Rajoitukset, kun lykättyä hyllytyskäsittelyä ei käytetä

On olemassa useita skenaarioita, joissa lykättyä hyllytystä ei käytetä, vaikka käytäntö on konfiguroitu. Seuraavassa on muutamia esimerkkejä:

- Manuaalista työn valmistumista käytetään.
- Työ saadaan valmiiksi automaattisen täydennyksen avulla.
- Valvontamalleja käytetään.


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>Lähtevän työn valvonta -työtilan lykättyjen käsittelytehtävien valvominen

**Lähtevän työn valvonta** -työtilassa on kaksi ruutua, joiden avulla voit valvoa lykättyjen käsittelytehtävien suorittamista:

- **Epäonnistuneet lykätyt hyllytyksen käsittelytehtävät** – tässä ruudussa näkyy epäonnistuneiden tehtävien määrä. Jos päonnistuneita tehtäviä ei ole, varastopäällikön on joko käsiteltävä ne uudelleen tai peruutettava ne, koska niitä ei käsitellä automaattisesti uudelleen.
- **Odottaa lykättyjä hyllytyksen käsittelytehtäviä** – tässä ruudussa näkyy niiden tehtävien määrä, jotka ovat olleet **Odottaa**-tilassa yli 10 minuutin ajan. Jos ruudussa näkyy numero, se saattaa ilmaista, että eräkäsittelyn aikana ilmeni ongelma. **Odottaa**-tehtävät voidaan käsitellä manuaalisesti. Jos tehtävän erätyö käsitellään myöhemmin, se epäonnistuu, koska se on jo käsitelty. Ei tule mitään vaikutusta.

## <a name="deleting-completed-tasks"></a>Poista suoritetut tehtävät

Voit poistaa lykätyt hyllytyksen käsittelytehtävät, jotka on suoritettu, valitsemalla ne ja poistamalla ne sivulta.

## <a name="additional-resources"></a>Lisäresurssit

- [Manuaalisen varastosiirtotoiminnon lykätty käsittely](deferred-processing-manual-inventory-movement.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]