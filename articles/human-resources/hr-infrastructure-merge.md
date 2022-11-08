---
title: Dynamics 365 Human Resources -infrastruktuurin yhdistämisen yleiskatsaus
description: Tässä artikkelissa kuvataan Microsoft Dynamics 365 Human Resources -infrastruktuurin yhdistäminen.
author: twheeloc
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f79ef3ed5db7583eb44b99e49c010778ce8524d1
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733450"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources -infrastruktuurin yhdistäminen 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamics Human Resources 365

Microsoft Dynamics 365 Human Resources sisältää työkaluja, joiden avulla HR-tiimit parantavat organisaation ketteryyttä, uudistavat työntekijäkokemuksen ja optimoivat HR-ohjelmat sekä luovat tällä tavoin työpaikan, jossa ihmiset ja liiketoiminta kukoistavat. Lisätietoja Dynamics 365 Human Resourcesissa on kohdassa [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Uudista työntekijäkokemus.** Tehokkaimmat työntekijät säilytetään tukemalla esihenkilöitä ja työntekijöitä yhdistettyjen osallistamista ja kasvua edistävillä itsepalvelukokemuksilla.
- **HR-ohjelmien optimointi.** Auta vähentämään operatiivisia kustannuksia ja luo ihmiskeskeisiä lomien, poissaolojen, työaikojen, etujen ja kompensaatioiden hallintaohjelmia.
- **Organisaation ketteryyden lisääminen.** Henkilöstöhallinto voi toimia ketterästi liiketoiminnan sitä edellyttäessä käyttämällä Dataversea ja Microsoft Power Platformia keskittämään ihmisiä koskevat tiedot sekä laajentamaan kätevästi Dynamics 365 Human Resourcesia.
- **Työvoimaa koskevien merkityksellisten tietojen löytäminen.** Tietopohjaisia päätökset voivat perustua ihmisiä koskevien tietojen analysointiin ja visualisointiin monipuolisissa koontinäytöissä, joita voi kaikenlaisissa laitteissa.

## <a name="human-resources-infrastructure-merge"></a>Human Resources -infrastruktuurin yhdistäminen

Dynamics 365 Human Resources on itsenäinen sovellus, joka käyttää tällä hetkellä eri infrastruktuuria kuin muut talous- ja toimintosovellukset, kuten Dynamics 365 Finance tai Dynamics 365 Supply Chain Management. Infrastruktuurin yhdistäminen tuo Dynamics 365 Human Resourcesin samaan infrastruktuuriin muiden talous- ja toimintosovellusten kanssa.

Lisätietoja Human Resources -infrastruktuurin yhdistämisestä on kohdassa [HR-tuotteiden yhdistäminen](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/). Katso vastauksia usein kysyttyihin kysymyksiin kohdasta [Human Resources -infrastruktuurin yhdistämisen usein kysytyt kysymykset](./hr-infrastructure-merge-faq.md).

## <a name="customer-migration-vs-customer-merge"></a>Asiakkaan siirto vs. asiakkaan yhdistäminen

Osana infrastruktuurin yhdistämistä, kaikki Human Resources -sovelluksen ominaisuudet ovat nyt käytettävissä talous- ja toimintosovellusympäristöissä. Asiakkaat voivat siirtää Human Resources -ympäristönsä käyttämällä Microsoft Dynamics Lifecycle Services -portaalissa käytettävissä olevia siirtotyökaluja. He voivat yhdistää tietonsa halutessaan myös nykyiseen talous- ja toimintosovellusympäristöönsä. 

Asiakkaan siirto ja asiakkaan yhdistäminen eroavat toisistaan seuraavin tavoin:

- **Asiakkaan siirto** – Automaattisia siirtotyökaluja käytetään suorittamaan "nosta ja siirrä" -tyylinen operaatio, jossa asiakastietokanta siirretään Human Resources -infrastruktuurista talous- ja toimintosovellusinfrastruktuuriin. Tuloksena on uusi talous- ja toimintosovellusympäristö, joka käyttää asiakkaan HR-tietokantaa. 
- **Asiakkaan yhdistäminen** – Microsoft ei vaadi tätä lisävaiheen suorittamista. Se tehdään asiakkaan oman harkinnan ja aikataulun mukaan. Tämän vaiheen aikana asiakastiedot siirretään olemassa olevaan ympäristöön, kuten Finance- tai Project Operations -ympäristöön. Se tapahtuu pääosin manuaalisesti, ja sen voi tehdä Data Management Frameworkin (DMF) tietoentiteettien avulla. 

## <a name="planning-a-human-resources-environment-migration"></a>Human Resources -ympäristön siirron suunnittelu

Kaikkien asiakkaiden täytyy siirtää nykyinen Human Resources -ympäristönsä erillisestä infrastruktuurista osana infrastruktuurin yhdistämistä. Suosittelemme tätä prosessia varten, että siirrät nykyiset ympäristösi uuteen infrastruktuuriin Lifecycle Services -portaalin automaattisten siirtotyökalujen avulla. 

Seuraavissa osiossa on lisätietoja Lifecycle Services -työkalujen käytöstä erillisen Human Resources -ympäristön siirtämiseen. 

Siirtoa suunnittelevilla asiakkailla voi olla seuraavat odotukset:

- Kaikkien asiakkaiden on siirrettävä eristysympäristö ennen kuin tuotantoympäristö voidaan siirtää. 
- Siirtotyökalu sallii siirron vain eristysympäristöstä eristysympäristöön ja tuotantoympäristöstä tuotantoympäristöön. Näin ollen ympäristön tyyppi määrittää, mikä ympäristö voidaan siirtää asianmukaisesti. 
- Asiakkaat voivat siirtää niin monta eristysympäristöä kuin on tarpeen ennen kuin he siirtävät tuotantoympäristönsä, mikäli eristysympäristön paikka on käytettävissä. Asiakkaat voivat myös poistaa siirretyn eristysympäristön ja suorittaa siirron uudelleen useita kertoja. 
- Jos eristysympäristön siirto epäonnistuu tai haluat aloittaa alusta, voit poistaa ympäristön talous- ja toimintosovellusinfrastruktuurista ja siirtää saman ympäristön uudelleen.
- Human Resources -ympäristösi URL-osoite muuttuu siirron yhteydessä.
- Varaa tarpeeksi aika palvelukatkokseen, kun siirrät tuotantoympäristösi. Automatisoidun siirtoprosessin suorittaminen kestää arviolta 3–4 tuntia. Kesto vaihtelee organisaatiosi tietojen mukaan. Sinun tulisi vahvistaa eristysympäristöjesi siirtämiseen tarvittava kesto ja varata aikaa mahdollisesti vaadituille manuaalisille lisätehtäville.

> [!IMPORTANT] 
> Kun tuotantoympäristö siirretään onnistuneesti talous- ja toimintosovellusinfrastruktuuriin, erillinen lähdetuotantoympäristö poistetaan automaattisesti. Sinun ei tulisi poistaa siirrettyä tuotantoympäristöä. 

Siirtoprosessi tapahtuu enimmäkseen automaattisesti. Yrityskäyttäjiesi täytyy kuitenkin suorittaa joitakin manuaalisia tehtäviä sekä vahvistus siirron jälkeen.

Seuraavat manuaaliset tehtävät täytyy suorittaa:

- Luo uusi Lifecycle Services -projekti siirtoa varten.
- Korjaa kaikki vanhan ympäristösi integraatiot toimimaan uudessa ympäristössä määrittämällä integraatio viittamaan uusiin URL-osoitteisiin/päätepisteisiin kunkin integraation kokoonpanon perusteella.
- Päivitä tietosäilö upotettuja Power BI -raportteja varten.
- Päivitä tietoyksiköiden luettelo DMF-työtilasta.
- Lifecycle Services -ohjelinkki.
- Luo kirjanpidon vuosikalentereita.

Automaattisen prosessin aikana suoritetaan seuraavat toimenpiteet, jotka tulisi tarkistaa:

- Tiedot:

    - Konfiguraatiot
    - Käyttöoikeusroolit (mukaan lukien mukautetut roolit)
    - Työnkulut
    - Mukautukset ja tallennetut näkymät
    - Tapahtumat
    - Mukautetut kentät
    - Liitteet

- Tiedonhallinta – Tuo oma tietokantasi (BYOD).
- Ominaisuuksien hallinta – Käyttöön otetut / käytöstä poistetut ominaisuudet.
- Upotettu Power Apps.
- Ympäristöön (vain tuotanto) liitetty Power Platform -hallintakeskus.
- Erätyöt.
- Jokaiselle yritykselle luodaan tyhjä kirjanpito. Jokaiselle kirjanpidolle määritetään oletusarvoinen vaihtokurssin tyyppi ja kirjanpitovaluutta.
- Uusi tilikartta luodaan automaattisesti ja linkitetään kunkin yrityksen **Kirjanpito**-sivulle. Human Resources -ympäristössäsi määritetyt taloushallinnon dimensiot lisätään automaattisesti uuteen tilirakenteeseen ja linkitetään kirjanpitoon. 

> [!NOTE]
> Kirjanpito on pakollinen talous- ja toimintosovellusinfrastruktuurissa osana Dynamics 365 Finance -tuotetta. Mukautettu dimension ohjausobjekti, joka oli käytettävissä erillisessä Dynamics 365 Human Resources -sovelluksessa, ei ole käytettävissä. Yhdistetty Human Resources -infrastruktuuri on riippuvainen Financen logiikasta näyttääkseen taloushallinnon dimensiot **Human Resources** -moduulissa. Löydät lisätietoja tilikartasta ja taloushallinnon dimensioista [täältä](../finance/general-ledger/plan-chart-of-accounts.md). 

## <a name="considerations"></a>Huomioitavat asiat

- Siirtyminen ympäristöihin tapahtuu aina uusimpaan yleisesti saatavilla olevaan versioon. Riippuen siirto- ja testaussuunnitelmasi, jos eristysympäristöjen siirron vahvistus suoritettiin eri versiolle, suosittelemme, että vahvistat eristysympäristön siirron samalla versiolla kuin tuotantoympäristösi. 
- Siirretyt ympäristöt asetetaan siirron aikana samalle alueelle kuin erilliset Human Resources -eristysympäristöt.

## <a name="licensing"></a>Käyttöoikeudet

Dynamics 365 Human Resources -lisensseihin ei tehdä muutoksia seuraavien osa-alueiden osalta: 

- **Ostettujen lisenssien vaadittu vähimmäismäärä**
- **Tuotanto- ja eristysympäristön käyttöoikeudet** – Jos sinulla on itsenäisiä Human Resources -lisenssejä, jotka myöntävät yhden tuotantoympäristön ja yhden eristysympäristön, talous- ja toimintosovellusinfrastruktuurissa on saatavilla sama määrä lisenssejä ilman lisämaksua.
- **Eristysympäristöjen lisälisenssit** – Jos olet ostanut eristysympäristöjen lisälisenssejä erilliselle Human Resources -sovellukselle, vakiohyväksynnän testiympäristölle (eristysympäristölle) on saatavilla sama määrä eristysympäristöjen lisenssejä talous- ja toimintosovellusinfrastruktuurissa ilman lisämaksua. 
