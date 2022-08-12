---
title: Store Commercen määritys- ja asennusongelmien vianmääritys
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Commerce Store Commerce -sovelluksen määritys- ja asennusongelmien vianmäärityksestä.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8af2c476ced05fc159a53131f8b51ad914a6c7c3
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168944"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Store Commercen määritys- ja asennusongelmien vianmääritys

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja Microsoft Dynamics 365 Commerce Store Commerce -sovelluksen määritys- ja asennusongelmien vianmäärityksestä.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>En voi aktivoida sovellusta, ja näyttöön tulee yhteyden virhesanoma

Kun olet kirjoittanut kelvollisen CPOS (Cloud Point of Sale) -URL-osoitteen, näyttöön voi tulla seuraavan esimerkin kaltainen yhteysvirheilmoitus:

> Yhteysvirhe on ilmennyt, eikä laite voi muodostaa yhteyttä CPOS:sään. Kirjoitetussa CPOS-URL-osoitteessa voi olla ongelmia.

Tarkista tässä tapauksessa URL-osoitteen kirjoitusvirheet. Voit myös määrittää, johtuuko yhteysongelma siitä, että CPOS on offline-tilassa.

Tarkista myös, että CSU (Cloud Scale Unit) -versio on 10.0.25 (9.35.\*.\*) tai uudempi. Store Commerce -sovelluksen käyttäminen edellyttää CPOS-versiota 10.0.25 tai uudempaa.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Sovelluksen asentaminen ei ole mahdollista, koska Moderni myyntipiste on jo asennettu.

Seuraava virhesanoma saattaa tulla näyttöön asennuksen aikana:

> Tämän tuotteen versio (9.\*.\*.\*) (Moderni myyntipiste) on aiemmin asennettu vanhalla asennusohjelmalla.

Voit korjata virheen poistamalla Moderni myyntipiste (MPOS) -sovelluksen kaikilta koneen käyttäjiltä ja yrittämällä sitten uudelleen. Voit vahvistaa, onko MPOS-tiedot poistettu kaikilta käyttäjiltä suorittamalla seuraavan PowerShell-komennon.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Sovellusta ei voi aktivoida virheellisen URL-osoitteen tai virhetilan vuoksi

Jos lisäämäsi CPOS-URL-osoite ei ole kelvollinen ja haluat muuttaa sitä tai jos Store Commerce -sovellus on virhetilassa aktivoinnin aikana, voit käynnistää prosessin uudelleen nollaamalla sovelluksen. Store Commerce -sovellus tallentaa vain kelvollisen CPOS-URL-osoitteen.

Voit nollata Store Commerce -sovelluksen noudattamalla seuraavia vaiheita.

1. Valitse sovellus Windowsin **Käynnistä**-valikosta ja pidä sitä painettuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse sitten **Lisää \> sovellusasetuksia**.
2. Selaa alaspäin sovelluksen asetussivua, kunnes löydät **Nollaa**-painikkeen.
3. Valitse **Nollaa**. Vahvista, että haluat nollata sovelluksen, kun sinua pyydetään tekemään niin.
