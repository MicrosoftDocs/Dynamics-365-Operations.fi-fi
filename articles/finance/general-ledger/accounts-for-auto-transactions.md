---
title: Automaattisten tapahtumien tilit
description: Tässä aiheessa kuvataan, kuinka automaattisten tapahtumien tilejä käytetään kirjattaessa Microsoft Dynamics 365:n kautta, sekä esimerkkejä automaattisten tapahtumien avaintileistä.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 275c74d673d1ba2468e23c5fa443c9272d13a184
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735257"
---
# <a name="accounts-for-automatic-transactions"></a>Automaattisten tapahtumien tilit

**Tilit automaattisia tapahtumia varten** -sivulla (**Kirjanpito &gt; Kirjausten määritys &gt; Tilit automaattisia tapahtumia varten**) määritellään oletuspäätili, jota käytetään järjestelmän jokaiselle kirjaustyypille. Vaikka useimmat kirjaustyypit voidaan määrittää moduuli- tai toimintokohtaisille sivulle, kirjaustyyppejä voi määrittää vain **Automaattisten tapahtumien tilit** -sivulla.

Voit esimerkiksi määrittää päätilin, jota käytetään **asiakkaan saldon** kirjaustyypille **Asiakkaan kirjausprofiili** -sivun **Yhteenveto**-kentässä, ja käyttää eri päätiliä jokaisessa asiakasprofiilissa. Näin voit hallita kirjauksia tarkemmin. Voit toisaalta määrittää nämä virhetilit vain **Automaattisten tapahtumien tilit** -sivulla.

Kun avaat uuden yrityksen **Automaattisten tapahtumien tilit** -sivun, tililuettelo on tyhjä. Voit lisätä useimmin sivulla konfiguroitavat kirjaustyypit valitsemalla **Luo oletustyypit** -painikkeen. Sen jälkeen voit jokaisella rivillä valita päätilin **Päätili**-kentästä. Jos jätät kirjaustyypin **päätilin** kentän tyhjäksi etkä ole konfiguroinut päätiliä moduuli- tai toimintokohtaisille sivulle, saat virhesanoman, kun kirjaat kirjaustyyppiä käyttävän tapahtuman. Yleensä sanoma on seuraava: "\[Kirjaustyypin\] tiliä ei löydy."

## <a name="default-posting-types"></a>Oletuskirjaustyypit

Seuraavassa taulukossa on esimerkkejä oletuskirjaustyypeistä, jotka luodaan, kun **automaattisten tapahtumien tilit** -sivulla valitaan **Luo oletustyypit**. Se näyttää päätilien otantatiedot ja kuvaukset. Veloitus/hyvitys? -sarake ilmaisee, kirjaako tapahtuma tavallisesti veloituksen vai hyvityksen. Joissakin tapauksissa tapahtuma voi kirjata joko veloituksen tai hyvityksen. Selvitystili-sarake ilmaisee, onko kirjaustyyppi selvitystili. Jos kirjaustyyppi on selvitystili, tilille kirjattu summa peruutetaan automaattisesti, kun myöhempi tapahtuma kirjataan.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Pyöristysero raportointivaluutassa | 618160 | Muu kulu | Kulut | Molemmat | Ei | Tätä kirjaustyyppiä käytetään, kun tapahtuman summa muunnetaan raportointivaluutaksi, kun tapahtuman summa muunnetaan ulkomaan valuuttana. |
| Pyöristysero kirjanpitovaluuttana | 618160 | Muu kulu | Kulut | Molemmat | Ei | Tätä kirjaustyyppiä käytetään, kun tapahtuman summa muunnetaan kirjanpitovaluutaksi, kun tapahtuman summa muunnetaan ulkomaan valuuttana. |
| Virhetili | 999999 | Virhetili | Kulut | Molemmat | Ei | Tätä kirjaustyyppiä käytetään, kun järjestelmässä tapahtuu virhe. Tili on vahvistettava joka kausi, ja mahdolliset virheet on korjattava. |
| Vuoden lopun tulos | 300160 | Jakamaton voitto | Oma pääoma | Molemmat | Ei | Tätä kirjaustyyppiä käytetään, kun vuoden lopun sulkemisprosessi suoritetaan **tulos**-tyypin tilien saldon siirtoa varten päätilille, joka on valittu vuoden lopputulosta varten. |
| Asiakkaan käteisalennus | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei | **Automaattisten tapahtumien tilit** -sivulla määritettyä kirjaustyyppiä ei käytetä. Päätili on pakollinen, kun käteisalennukset määritetään myyntireskontrassa.|
| Toimittajan käteisalennus | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei | **Automaattisten tapahtumien tilit** -sivulla määritettyä kirjaustyyppiä ei käytetä. Päätili on pakollinen, kun käteisalennukset määritetään ostoreskontrassa. |

## <a name="additional-posting-types"></a>Lisäkirjaustyypit

Seuraavassa taulukossa on esimerkkejä lisäkirjaustyypeistä, jotka on konfiguroittava, jos aiot käyttää liittyviä toimintoja. Näiden kirjaustyyppien kirjausprofiilin konfiguraatiota ei voi käyttää toisessa moduulissa. Veloitus/hyvitys? -sarake ilmaisee, kirjaako tapahtuma tavallisesti veloituksen vai hyvityksen. Joissakin tapauksissa tapahtuma voi kirjata joko veloituksen tai hyvityksen. Selvitystili-sarake ilmaisee, onko kirjaustyyppi selvitystili. Jos kirjaustyyppi on selvitystili, tilille kirjattu summa peruutetaan automaattisesti, kun myöhempi tapahtuma kirjataan.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Konsolidointieron tasetili | 801200 | Voitto ja tappio - uudelleenarvostus | Kulut | Molemmat | Ei | Tätä kirjaustyyppiä käytetään, kun suoritat konsolidoinnin, johon liittyy valuutan uudelleenarvostus, ja uudelleenarvostuksen aikana tapahtuu sentin eroja. |
| Voitto- ja tappiotili konsolidointieroja varten | 801200 | Voitto ja tappio - uudelleenarvostus | Kulut | Molemmat | Ei | Tätä kirjaustyyppiä käytetään, kun suoritat konsolidoinnin, johon liittyy valuutan uudelleenarvostus, ja uudelleenarvostuksen aikana tapahtuu sentin eroja. |
| Yksiköiden välinen – debet | 133500 | Yksikön välinen saatava | Resurssi | Debit | Ei | Tätä kirjaustyyppiä käytetään, kun valitset **kirjanpito**-sivulta täsmäyttävän dimension eikä kirjatun tapahtuman dimensio täsmää. |
| Yksiköiden välinen – kredit | 233500 | Yksikön välinen maksu | Velat | Luotto | Ei | Tätä kirjaustyyppiä käytetään, kun valitset **kirjanpito**-sivulta täsmäyttävän dimension eikä kirjatun tapahtuman dimensio täsmää. |
