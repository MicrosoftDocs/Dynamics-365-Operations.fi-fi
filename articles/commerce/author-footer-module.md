---
title: Alatunnistemoduuli
description: Tässä artikkelissa on tietoja alatunnistemoduuleista ja niiden muokkaamisesta Microsoft Dynamics 365 Commerce -sovelluksessa.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: fefeed37ba0d0e800b9cd3cefcf207cde9a625d8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282954"
---
# <a name="footer-module"></a>Alatunnistemoduuli  

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja alatunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.

Alatunnistemoduuli on erillinen säilö, jota käytetään sivun alatunnisteessa näkyvien moduulien isännöintiin. Se voi esimerkiksi sisältää linkkejä eri sivuston sivuille. Sivu voi olla esimerkiksi **Ota yhteyttä** tai **Myymälän käytännöt**.

Seuraavassa kuvassa on esimerkki alatunnistemoduulista sivuston sivulla.

![Esimerkki alatunnistemoduulista.](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Ylätunnistemoduulin ominaisuudet 

Useimpien säilöjen tapaan alatunnistemoduuli tukee otsikon ja leveyden ominaisuuksia. Se tukee myös useiden alatunnisteluokkamoduulien lisäämistä. Jokainen lisätty alatunnisteluokkamoduuli hahmonnetaan sarakkeeksi alatunnistemoduuliin.

## <a name="modules-available-in-a-footer-module"></a>Alatunnistemoduulissa käytettävissä olevat moduulit

**Alatunnistenimike** – Alatunnistenimikkeiden moduuli voi sisältää otsikon tai linkin. Otsikkoa käytetään yleensä alatunnisteen osan otsikkona.  Jokainen alatunnisteen linkki voidaan määrittää siten, että siinä on vain teksti (esimerkiksi Ota yhteyttä ja Tietosuojalinkit) tai niin, että sillä on sekä tekstiä että kuva (esimerkiksi yhteisöpalveluiden linkit). Jos sekä otsikko että linkki ovat käytettävissä, otsikko-ominaisuuden arvo ohittaa linkin. 

**Palaa alkuun** – Palaa alkuun -moduuli sisältää linkin, jonka avulla voi siirtyä nopeasti sivun yläreunaan. Kohde on määritettävä. Kohteen oletusarvo on \#. Se vie käyttäjän sivun yläosaan.

## <a name="create-a-footer-module"></a>Alatunnistemoduulin lisääminen

1. Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.
1. Valitse **Valitse katkelma** -valintaikkunassa **Kontti**-moduuli. Syötä osan nimi ja valitse **OK**.
1. Valitse kolme pistettä (**...**) **Oletuskontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Alatunnisteluokka**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Alatunnisteluokka**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Alatunnistenimike**-moduuli ja valitse sitten **OK**.
1. Valitse **Alatunnistenimike**-paikka ja määritä sitten oikeanpuoleisessa ominaisuusruudussa otsikko, linkki, linkin teksti ja kuvat halutulla tavalla.
1. Voit lisätä alatunnistenimikkeitä toistamalla kullekin kohtien 5–7 toimet.
1. Voit lisätä Palaa alkuun -linkin alatunnisteeseen valitsemalla **Alatunnisteluokka**-paikka jäsennyspuussa kolmen pistettä (**...**) ja valitsemalla sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Takaisin ylös**-moduuli ja valitse sitten **OK**.
1. Valitse **Palaa alkuun**-paikka ja määritä sitten oikeanpuoleisessa ominaisuusruudussa teksti ja muut moduuliominaisuudet halutulla tavalla.
1. Valitse **Lopeta muokkaus** tallentaaksesi osan ja valitse sitten **Julkaise** julkaistaksesi sen.

Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.

1. Lisää **Alatunniste**-moduulin **Otsikko**-paikkaan alatunnistemoduulissa luomasi alatunnisteosa.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.

Kun lisäät sivumalleihin osan, voit varmistaa, että alatunniste hahmonnetaan jokaiselle sivulle.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
