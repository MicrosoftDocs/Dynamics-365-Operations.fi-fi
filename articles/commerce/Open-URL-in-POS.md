---
title: URL-osoitteen avaaminen myyntipisteessä
description: Tämä artikkeli sisältää yleiskatsauksen parannuksista, jotka on tehty Dynamics 365 Commercen tuote- ja asiakashakuihin.
author: ShalabhjainMSFT
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.custom: 141393
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: ad82cf1039515e58d1717453ee3fb4e3dafd84fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276424"
---
# <a name="open-url-in-pos"></a>URL-osoitteen avaaminen myyntipisteessä

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Dynamics 365 Commerce -myyntipisteessä (POS) voi määrittää painikkeen avaaman URL-osoitteen. Tätä ominaisuutta varten ei tarvitse muokata koodia ja sen voi määrittää myös henkilö, jolla ei ole kehittäjän roolia. 

Tällä ominaisuudella voi määrittää POS:n painikkeen avaamaan URL-osoitteen käyttämällä painikeruudukon suunnittelutoimintoa. Ominaisuutta tuetaan tällä hetkellä seuraavissa määrityksissä:

- Avaa uudessa ikkunassa.
- Avaa POS-sovelluksessa.
- Avaa alkuperäinen sovellus.

## <a name="open-in-new-window"></a>Avaa uudessa ikkunassa

Tämä määritys määrittää, avataanko URL-osoite uudessa ikkunassa tai sovelluksessa. Jos URL-osoite on määritetty avautumaan sovelluksessa, reunan siirtymispaneeli ja POS-yläpalkki ovat näkyvissä ja käyttäjän käytettävissä. Jos URL-osoite on määritetty avautumaan uudessa ikkunassa, URL avautuu uudessa sovellusikkunassa tai Modern POS for Windowsissa ja uudessa selainvälilehdessä kaikissa muissa POS-asiakasohjelmissa. Voit ottaa ominaisuuden käyttöön määrittämällä URL-osoitteen siten, että **Avaa uudessa ikkunassa** -asetus on valittu.

## <a name="open-within-pos"></a>Avaaminen POS-sovelluksessa

URL-osoitteen avaamista POS-sovelluksessa tuetaan tällä hetkellä vai Modern POS for Windowsissa. Tätä toimintoa kehitetään vielä muissa asiakasohjelmissa, ja sen julkaisu on suunniteltu tuleviin päivityksiin. Voit ottaa ominaisuuden käyttöön määrittämällä URL-osoitteen siten, että **Avaa uudessa ikkunassa** -asetusta ei ole valittu.

## <a name="open-a-native-app"></a>Alkuperäisen sovelluksen avaaminen

Tällä ominaisuudella voi määrittää myös verkon ulkopuoliset URL-osoitteet avaa alkuperäisen sovelluksen. Voit esimerkiksi määrittää URL-protokollat, kuten MailTo, SIP, IM tai MSTEAMS, joita voidaan käsitellä kunkin protokollan alkuperäisellä sovelluksella isäntälaitteessa. Voit ottaa ominaisuuden käyttöön määrittämällä URL-osoitteen siten, että **Avaa uudessa ikkunassa** -asetus on valittu.

- Lisätietoja Windows-tietokoneita koskevista oletusprotokollaliitoksista, jos tietokone määritetään DISM:n (Deployment Image Servicing and Management) avulla, on kohdassa [Sovelluksen oletusliitosten vienti tai tuonti](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).
- Jos Windows-tietokoneiden hallintaan käytetään MDM:ää, kuten Intunea, lisätietoja on kohdassa [CSP-käytäntö – ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).
- Jos olet mukautettua sivustoa rakentava kehittäjä, katso [URI:n oletussovelluksen käynnistäminen](/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Alkuperäisen sovelluksen sujuva avaaminen

Windows, iOS ja Android sallivat lisäksi sovellusten entistä sujuvamman avaamisen sovelluksen protokollaliitoksen perusteella. Jos sovellusta ei ole vielä määritetty käsittelemään avaamista selaimesta, kehittäjän on ehkä määritettävä tämä.

- Windows: katso [Sovellusten käyttöönotto sivustoja varten sovelluksen URI-käsittelijöiden avulla](/windows/uwp/launch-resume/web-to-app-linking).
- iOS: katso [Kehittäjien yleiset linkit](https://developer.apple.com/ios/universal-links/).
- Android: katso [Android-sovelluksen linkkien käsitteleminen](https://developer.android.com/training/app-links/).

| Asiakas                | Avaa uudessa ikkunassa | Alkuperäisen sovelluksen avaaminen | Avaaminen POS-sovelluksessa | Yksityiskohdat                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Windowsin Modern POS | ✓\*                | ✓               | ✓              | \* Avautuu uudessa Modern POS -ikkunassa |
| Cloud POS             | ✓\*                | ✓               | X              | \* Avautuu uudessa selainvälilehdessä        |
| iOS:n Modern POS     | ✓\*                | ✓               | X              | \* Avautuu uudessa selainvälilehdessä        |
| Modern POS:n Android-versio | ✓\*                | ✓               | X              | \* Avautuu uudessa selainvälilehdessä        |

## <a name="before-you-begin"></a>Ennen aloittamista

Tarkista ennen aloittamista, miten [myyntipisteen (POS) näytön asettelut](pos-screen-layouts.md) määritetään.

## <a name="open-url-in-pos"></a>URL-linkin avaaminen POS-sovelluksessa

Määritä URL-osoite avautumaan POS:ssä seuraavien ohjeiden mukaan.

1. Valitse pääkonttorissa **Vähittäismyynti ja kauppa \> Kanavan asetukset \> POS-asetukset \> Myyntipiste \> Näytön asettelut**.
2. Valitse **Painikeruudukot \> Suunnittelutoiminto**.
3. Luo uusi painike.
4. Valitse **Painikeominaisuudet**.
5. Valitse **Avaa URL** toimintona.
6. Anna käytettävä URL-osoite.
7. Määritä, avataanko URL-osoite uudessa ikkunassa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
