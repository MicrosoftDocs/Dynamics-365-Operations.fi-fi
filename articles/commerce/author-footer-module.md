---
title: Alatunnistemoduuli
description: Tässä ohjeaiheessa on tietoja alatunnistemoduuleista ja niiden muokkaamisesta Microsoft Dynamics 365 Commerce -sovelluksessa.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c253cd9620180b09f2f5cae232e46d236deabdd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697310"
---
# <a name="footer-module"></a>Alatunnistemoduuli  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja alatunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.

## <a name="overview"></a>Yleiskatsaus

Alatunnistemoduuli on erillinen säilö, jota käytetään sivun alatunnisteessa näkyvien moduulien isännöintiin. Se voi esimerkiksi sisältää linkkejä eri sivuston sivuille. Sivu voi olla esimerkiksi **Ota yhteyttä** tai **Myymälän käytännöt**.

## <a name="footer-module-properties"></a>Ylätunnistemoduulin ominaisuudet 

Useimpien säilöjen tapaan alatunnistemoduuli tukee otsikon ja leveyden ominaisuuksia. Se tukee myös useiden alatunnisteluokkamoduulien lisäämistä. Jokainen lisätty alatunnisteluokkamoduuli hahmonnetaan sarakkeeksi alatunnistemoduuliin.

## <a name="modules-available-in-a-footer-module"></a>Alatunnistemoduulissa käytettävissä olevat moduulit

**Alatunnistenimikkeet** – Alatunnistenimikkeiden moduuli voi sisältää otsikon, kuvan ja linkin. Otsikkoa voidaan käyttää yksin tai yhdessä kuvan ja linkin kanssa. Jokainen alatunnisteen linkki voidaan määrittää siten, että siinä on vain teksti (esimerkiksi Ota yhteyttä ja Tietosuojalinkit) tai niin, että sillä on sekä tekstiä että kuva (esimerkiksi yhteisöpalveluiden linkit).

**Palaa alkuun** – Palaa alkuun -moduuli sisältää linkin, jonka avulla voi siirtyä nopeasti sivun yläreunaan. Kohde on määritettävä. Kohteen oletusarvo on #. Se vie käyttäjän sivun yläosaan.

## <a name="author-a-footer-module"></a>Alatunnistemoduulin muokkaaminen

1. Valitse siirtymisruudussa **Osat** ja valitse sitten **Uusi sivun osa**.
1. Valitse **Uusi sivun osa** -valintaikkunassa alatunnistemoduuli. Syötä sivun osan nimi ja valitse **OK**.
1. Valitse vasemmanpuoleisessa jäsennyspuussa alatunnistemoduulin kolmen pisteen painike (**...**) ja valitse **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa alatunnisteluokkamoduuli ja valitse sitten **OK**.
1. Valitse jäsennyspuussa alatunnisteluokkamoduulin kolmen pisteen painike (...) ja valitse **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa alatunnistenimikemoduuli ja valitse sitten **OK**.
1. Valitse jäsennyspuussa alatunnistenimikemoduuli. Määritä sitten oikeanpuoleisessa ominaisuusruudussa otsikko, linkki, linkin teksti ja kuvat haluamallasi tavalla.
1. Voit lisätä alatunnistenimikkeitä toistamalla kohtien 5–7 toimet.
1. Voit lisätä Palaa alkuun -linkin alatunnisteeseen valitsemalla alatunnisteluokkamoduulin jäsennyspuussa kolmen pisteen painikkeen ja valitsemalla sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa Palaa alkuun -moduuli ja valitse sitten **OK**.
1. Valitse jäsennyspuussa Palaa alkuun -moduuli. Määritä sitten oikeanpuoleisessa ominaisuusruudussa Palaa alkuun -moduuli haluamallasi tavalla.
1. Tallenna sivun osa, kirjaa se sisään ja julkaise se.

Noudata seuraavia vaiheita jokaiselle sivustolle luodulle sivumallille.

1. Lisää oletussivun **pääpaikkaan** alatunnistemoduulissa luomasi alatunnisteosa.
1. Tallenna malli, kirjaa se sisään ja julkaise se.

Kun lisäät sivumalleihin sivun osan, voit varmistaa, että alatunniste hahmonnetaan jokaiselle sivulle.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)