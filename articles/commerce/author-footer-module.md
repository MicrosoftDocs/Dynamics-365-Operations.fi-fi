---
title: Alatunnistemoduuli
description: Tässä ohjeaiheessa on tietoja alatunnistemoduuleista ja niiden muokkaamisesta Microsoft Dynamics 365 Commerce -sovelluksessa.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 87ffc0204019f2f7122c40dc21bdb5de012929d6
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411197"
---
# <a name="footer-module"></a>Alatunnistemoduuli  

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja alatunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.

## <a name="overview"></a>Yleiskatsaus

Alatunnistemoduuli on erillinen säilö, jota käytetään sivun alatunnisteessa näkyvien moduulien isännöintiin. Se voi esimerkiksi sisältää linkkejä eri sivuston sivuille. Sivu voi olla esimerkiksi **Ota yhteyttä** tai **Myymälän käytännöt**.

Seuraavassa kuvassa on esimerkki alatunnistemoduulista sivuston sivulla.

![Esimerkki alatunnistemoduulista](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Ylätunnistemoduulin ominaisuudet 

Useimpien säilöjen tapaan alatunnistemoduuli tukee otsikon ja leveyden ominaisuuksia. Se tukee myös useiden alatunnisteluokkamoduulien lisäämistä. Jokainen lisätty alatunnisteluokkamoduuli hahmonnetaan sarakkeeksi alatunnistemoduuliin.

## <a name="modules-available-in-a-footer-module"></a>Alatunnistemoduulissa käytettävissä olevat moduulit

**Alatunnistenimikkeet** – Alatunnistenimikkeiden moduuli voi sisältää otsikon, kuvan ja linkin. Otsikkoa voidaan käyttää yksin tai yhdessä kuvan ja linkin kanssa. Jokainen alatunnisteen linkki voidaan määrittää siten, että siinä on vain teksti (esimerkiksi Ota yhteyttä ja Tietosuojalinkit) tai niin, että sillä on sekä tekstiä että kuva (esimerkiksi yhteisöpalveluiden linkit).

**Palaa alkuun** – Palaa alkuun -moduuli sisältää linkin, jonka avulla voi siirtyä nopeasti sivun yläreunaan. Kohde on määritettävä. Kohteen oletusarvo on \#. Se vie käyttäjän sivun yläosaan.

## <a name="create-a-footer-module"></a>Alatunnistemoduulin lisääminen

1. Siirry kohtaan **Sivun osat** ja **Uusi** luodaksesi uuden osan.
1. Valitse **Uusi sivun osa** -valintaikkunassa **Kontti**-moduuli. Syötä sivun osan nimi ja valitse **OK**.
1. Valitse kolme pistettä (**...**) **Oletuskontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Alatunnisteluokka**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Alatunnisteluokka**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Alatunnistenimike**-moduuli ja valitse sitten **OK**.
1. Valitse **Alatunnistenimike**-paikka ja määritä sitten oikeanpuoleisessa ominaisuusruudussa otsikko, linkki, linkin teksti ja kuvat halutulla tavalla.
1. Voit lisätä alatunnistenimikkeitä toistamalla kullekin kohtien 5–7 toimet.
1. Voit lisätä Palaa alkuun -linkin alatunnisteeseen valitsemalla **Alatunnisteluokka**-paikka jäsennyspuussa kolmen pistettä (**...**) ja valitsemalla sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Palaa alkuun** -moduuli ja valitse sitten **OK**.
1. Valitse **Palaa alkuun**-paikka ja määritä sitten oikeanpuoleisessa ominaisuusruudussa teksti ja muut moduuliominaisuudet halutulla tavalla.
1. Valitse **Lopeta muokkaus** tallentaaksesi osan ja valitse sitten **Julkaise** julkaistaksesi sen.

Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.

1. Lisää **Alatunniste**-moduulin **Otsikko**-paikkaan alatunnistemoduulissa luomasi alatunnisteosa.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.

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
