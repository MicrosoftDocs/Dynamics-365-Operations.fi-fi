---
title: Toimitusalennus
description: Tässä artikkelissa kerrotaan toimitusalennusominaisuuksista Microsoft Dynamics 365 Commercessa ja asetuksista, jotka ominaisuuksien käyttöä varten vaaditaan.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: 74cfe5246ad72cbdedd0ed4e3b3394bf7277919e
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473847"
---
# <a name="shipping-discount"></a>Toimitusalennus

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan toimitusalennusominaisuuksista Microsoft Dynamics 365 Commercessa ja asetuksista, jotka ominaisuuksien käyttöä varten vaaditaan.

Ilmainen toimitus tai toimitus, josta annetaan alennusta, on eräs tekijä, joka vaikuttaa asiakkaiden verkko-ostopäätöksiin. Useat jälleenmyyjät käyttävät ilmaista toimitusta motivoidakseen asiakkaita ostoskorin koon ja samalla tapahtumakohtaisen tuoton kasvattamiseen.

Commerce tukee toimitusalennusominaisuutta, jonka avulla jälleenmyyjät voivat määrittää alennusprosentin toimituskuluille tietyssä toimitustavassa, kun tapahtuman hyväksyttyjen nimikkeiden kokonaismyyntisumma vastaa tiettyjä ehtoja. Esimerkki toimitusalennusta käyttävästä skenaariosta: Ilmainen toimitus seuraavana päivänä, jos tilaat tuotteita vähintään 50 € arvosta.

## <a name="prerequisites"></a>Edellytykset

Commercen [kaikkikanavaisen edistyneiden automaattisten kulujen](/dynamics365/unified-operations/retail/omni-auto-charges) toiminnot tukevat toimitusalennusominaisuutta. Jotta toimitusalennusominaisuus toimii, ota käyttöön **Käytä edistyneitä automaattisia kuluja** -määritys Commerce headquartersin **Commerce parameters** -sivun **Asiakastilaukset**-välilehdessä. Jälleenmyyjät voivat käyttää edistyneiden automaattisten kulujen toimintoa määrittäessään eri tyyppisiä kuluja, kuten käsittely-, asennus- ja poistokuluja.

Toimitusalennusta käytetään vain toimituskuluihin. Tämän vuoksi jälleenmyyjän on määritettävä, mitkä kulut ovat toimituskuluja. Voit määrittää toimituskulut siirtymällä Commerce headquartersissa kohtaan **Kanavan asetukset \> Kulut \> Kulujen koodi** ja määrittämällä haluttujen nimikkeiden **Toimituskulu**-vaihtoehdon arvoksi **Kyllä**.

![Kulun määrittäminen toimituskuluksi.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Konfiguraatio

Toimitusalennusominaisuus perustuu tasoihin ja tukee vain **Alennusprosentti**-laskentatyyppiä. Voit määrittää toimitusalennuksen Commerce headquartersissa siirtymällä kohtaan **Hinnoittelu ja alennukset \> Toimitusraja-alennus**. Tämän jälkeen voit määrittää toimitustavan, jota alennus koskee, vähintään yhden summaraja-arvon ja alennusprosentin jokaiselle raja-arvolle. Voit myös määrittää hyväksyttyjen nimikkeiden luokka- tai tuoteluettelon. Tämän jälkeen vain näiden nimikkeiden myyntisummat tapahtumassa lasketaan hinnoittelumoduulin arvioidessa, vastaako tapahtuman kokonaissumma raja-arvoa.

> [!NOTE]
> Toisin kuin muissa alennustyypeissä, toimitusalennus ei luo alennusrivejä. Sen sijaan se muokkaa toimituskulua suoraan ja liittää alennuksen nimen kulun kuvaukseen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
