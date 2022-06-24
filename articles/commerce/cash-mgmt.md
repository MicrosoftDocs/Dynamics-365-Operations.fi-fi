---
title: Kassanhallinnan parannukset
description: Tässä artikkelissa kuvataan Dynamics 365 Commerce -ohjelman käteisvarojen hallinnan (POS) parannuksia.
author: anpurush
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1719e309183042cd7f56be3df8cbbec31cea7c79
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849064"
---
# <a name="cash-management-improvements"></a>Kassanhallinnan parannukset

[!include [banner](includes/banner.md)]


Kassanhallinta on fyysisten myymälöiden vähittäiskauppiaiden keskeinen toiminto. Vähittäiskauppiaat haluavat, että heidän myymälöissään on järjestelmiä, joiden avulla he voivat tarjota käteisvarojen täydellisen jäljitettävyyden ja vastuullisuuden ja niiden liikkumisen eri kassakoneissa ja kassoilla myymälässä. Heidän on pystyttävä täsmäyttämään mahdolliset erot ja määriteltävä vastuullisuus.


Microsoft Dynamics 365 Commerceilla on kassanhallintatoimintoja myyntipisteen (POS) sovelluksessa. Kassanhallintatoiminnot eivät kuitenkaan ole riittävän vahvoja, jotta käteisvarojen liikkeet voidaan jäljittää täydellisesti, mikäli vähittäismyyntitoiminnot ovat versiota 10.0.3 vanhempia. Vaikka vähittäiskauppiaat voivat täsmäyttää myymälän käteisvarat, ne eivät voi tarkasti määrittää vastuullisuutta, jos käteisvarat poikkeavat toisistaan.


Retailin versiossa 10.0.3 ja sitä uudemmissa versioissa vähittäiskauppiaat saavat jäljitettävyyden käteisen käsittelyä varten. Osana tätä jäljitettävyyttä jälleenmyyjät voivat määrittää säilöt, tehdä kaksisuuntaisia käteistapahtumia ja täsmäyttää kassanhallintatapahtumat.

## <a name="set-up-traceability-and-define-safes"></a>Jäljitettävyyden luonti ja säilöjen määrittäminen

Voit määrittää uudet kassanhallintatoiminnot määrittämällä myymälöiden toimintoprofiilin seuraavasti.

1. Valitse **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit** ja valitse toimintoprofiili, joka on linkitetty myymälöihin, joille haluat tarjota kassanhallintatoimintojen parannukset.
2. Valitse toimintoprofiilin **Toiminnot**-pikavälilehden **Kehittynyt käteisvarojen hallinta** -kohdassa **Ota käyttöön käteisen jäljitettävyys** -asetukseksi **Kyllä**.
3. Määrittääksesi säilöt, mene kohtaan **Retail ja Commerce \> Kanavat \> Myymälät \> Kaikki myymälät** ja valitse sitten myymälä.
4. Valitse **Myymälät**-sivun toimintoruudun **Määritä**-välilehden **Määritä**-ryhmässä **Säilöt**. Tämän vaihtoehdon avulla voit määrittää myymälälle useita säilöjä ja ylläpitää niitä.
4. Ennen kuin toimintoja voi käyttää, sinun on synkronoitava **1070-kanavakonfiguraatio** tietokantaan suorittamalla kanavamääritysten jakelun ajoitustehtävä.

## <a name="additional-cash-management-changes"></a>Kassanhallinnan lisämuutokset

Retail-versiossa 10.0.3 ja uudemmissa on myös seuraavat käteistapahtumiin liittyvät ominaisuudet:

- Käyttäjän, jolle esitetään pyyntö "Ilmoita aloitussumma", on syötettävä käteisen lähde. Käyttäjä voi etsiä myymälästä määritettyjä käytettävissä olevia säilöjä ja valita säilön, joka on otettu pois käytöstä, jotta se voidaan kirjata rekisteriin.
- Käyttäjän, joka tekee maksuvälinepoistotoiminnon, tulee valita avointen liukuvien merkintätapahtumien luettelosta tapahtuma, johon työvaihe tehdään. Jos järjestelmässä ei ole vastaavaa liukuvaa merkintää, käyttäjä voi luoda ei-linkitetyn maksuvälineen poistotapahtuman.
- Liukuva merkintä -toiminto kehottaa käyttäjää valitsemaan avoimen maksuvälinepoistotoiminnon luettelossa tapahtuman, johon työvaihe tehdään. Jos järjestelmässä ei ole vastaavaa maksuvälineen poistoa, käyttäjä voi luoda ei-linkitetyn liukuvan merkinnän tapahtuman.
- Käyttäjältä, joka tekee toimituksen kassakaappiin, kysytään, haluatko valita säilön, johon käteinen toimitetaan.
- Kun säilöt on määritetty myymälässä, käyttäjät voivat hallita toimintoja, kuten määrittää aloitussumman, tehdä liukuvan merkinnän, maksuvälineen poiston ja toimituksen pankkiin.
- Jos käyttäjällä on tarvittavat käyttöoikeudet, työvuorojen ylläpito-operaatiot näyttävät aktiivisten, keskeytettyjen ja piilotettujen suljettujen vuorojen käteissaldot.
- Jos haluat täsmäyttää käteistapahtumat vuoron aikana tai vuorojen välillä, valitse täsmäytettävä vuoro ja sitten **Täsmäytä**. Avattava näkymä sisältää täsmäyttävien ja täsmäyttämättömien tapahtumien luettelon erillisillä välilehdillä. Tässä näkymässä käyttäjät voivat joko valita täsmäyttämättömiä tapahtumia ja täsmäyttää ne tai valita aiemmin täsmäyttämättömät tapahtumat ja poistaa niiden täsmäytyksen.
- Jos valitun tapahtuman saldo ei täsmää täsmäytyksen aikana, käyttäjän on kirjoitettava epätasapainoisen täsmäytyksen syyn kuvaus. Käyttäjät voivat valita yhden tapahtuman ja täsmäyttää sen asiaankuuluvan syyn kuvauksen kanssa.
- Käyttäjät voivat edelleen täsmäyttää ja purkaa tapahtumia, kunnes vuoro on suljettu. Kun vaihto on suljettu, tapahtumia ei voi täsmäyttää.
- Kun käyttäjä päättää vuoron sulkemisesta, Commerce tarkistaa, että vuorossa ei ole täsmäyttämättömiä kassanhallintatapahtumia. Käyttäjät eivät voi sulkea vuoroja, jos niissä on täsmäyttämättömiä tapahtumia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]