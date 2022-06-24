---
title: Ajoitettu suoritus
description: Tässä artikkelissa käsitellään ajoitettua suoritusta resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e9d6af5c224f683481378da57708fda3c1b7207
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848046"
---
# <a name="scheduled-execution"></a>Ajoitettu suoritus

[!include [banner](../../includes/banner.md)]

 

Voit määrittää ajoitetun suorituksen työtilauksen palvelutasojen avulla. (Lisätietoja työtilauksen palvelutasoista on kohdassa [Palvelutaso ja kuvaus](service-level-and-description.md).) Ajoitettu suorittaminen mahdollistaa kunnossapitotyöntekijöiden työsuunnittelun joustavuuden, sillä voit määrittää yksityiskohtaisempia tai vähemmän yksityiskohtaisia vaatimuksia sille aikavälille, jonka aikana työtilaus tulee suorittaa. Esimerkiksi huoltotyöntekijä, joka suorittaa työn valmiiksi odotettua nopeammin tuotantolaitoksessa, voi ehkä siirtyä toiseen läheiseen työhön, joka suunniteltiin nykyiselle viikolle, mutta ei välttämättä nykyiselle päivälle. Tämä lähestymistapa mahdollistaa työntekijöiden suunnittelun ja työn valmistumisen optimoinnin.

Työtilauksiin liittyvät ajoitetut suoritusmääritykset voivat olla yleisiä tai erityisiä. Voit määrittää yleisiä rivejä, jotka eivät rajoitu tiettyihin työtilaustyyppeihin, resursityyppeihin ja niin edelleen. Vaihtoehtoisesti voit luoda ajoitettuja suoritusrivejä, jotka koskevat tiettyä työtilaustyyppiä, käyttöomaisuuden tyyppiä, kunnossapitotöiden tyyppiä jne.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Ajoitettu suoritus**.
2. Luo ajoitettu suoritusrivi valitsemalla **Uusi**.
3. Valitse haluamasi arvot kentissä **Toiminnallinen sijainti**, **Työtilaustyyppi**, **Resurssin tyyppi**, **Valmistaja**, **Malli**, **Ylläpitotyön tyypin luokka**, **Ylläpitotyön tyyppi**, **Ylläpitotyön tyypin variantti** ja **Toimiala**.
4. Valitse **Palvelutaso**-kentässä työtilauksen palvelutaso. Jos jätät tämän kentän tyhjäksi, voit määrittää yleisen ajoitetun suorituksen rivityypin. Esimerkiksi yleisestä rivistä, on seuraavan kuvan ensimmäisessä tietueessa. Tämä rivi mahdollistaa sen, että kaikki työtilaukset, joilla ei ole työtilauksen palvelutasoa, ajoitetaan tietylle päivämäärälle ja kellonaikaan.
5. Valitse **Ajoitettu suoritus** -kentässä aikaväli.
6. Valitse **Tallenna**.

![Ajoitettu suoritus.](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]