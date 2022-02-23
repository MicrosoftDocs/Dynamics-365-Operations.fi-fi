---
title: Arvonlisäveron laskeminen online-tilauksille
description: Tässä ohjeaiheessa on yhteenveto eri online-tilaustyyppien arvonlisäveroryhmän valinnasta Dynamics 365 Commercessa.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 40c20bf13779f73289e43df21b763e1b864686a7
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530194"
---
# <a name="configure-sales-tax-for-online-orders"></a>Arvonlisäveron laskeminen online-tilauksille

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa on yhteenveto eri online-tilaustyyppien arvonlisäveroryhmän valinnasta. 

Sähköisen kaupankäynnin kanava voi tarvita tuen online-tilausten vaihtoehdoille, kuten toimittamiselle tai noudolle. Arvonlisäveron sovellettavuus perustuu online-käyttäjien valitsemaan vaihtoehtoon. Kun sivuston asiakas haluaa ostaa nimikkeen verkosta ja saada sen toimitetuksi osoitteeseen, arvonlisävero määräytyy asiakkaan toimitusosoitteen veroryhmän asetuksen mukaan. Kun asiakas päättää noutaa ostetun nimikkeen myymälästä, arvonlisävero määräytyy noutomyymälän veroryhmän asetuksen mukaan. 

## <a name="orders-shipped-to-a-customer-address"></a>Asiakkaan osoitteeseen toimitetut tilaukset 

Yleensä asiakkaan osoitteisiin toimitettavien online-tilausten verot määräytyvät määränpään mukaan. Jokaisella arvonlisäveroryhmällä on vähittäismyynnin määränpäähän perustuva verokonfiguraatio, jossa yrityksesi voi määrittää määränpään tiedot, kuten läänin/alueen, osavaltion, läänin ja kaupungin hierarkkisessa muodossa. Kun online-tilaus tehdään, Commercen veromoduuli käyttää jokaisen tilauksen rivinimikkeen toimitusosoitetta ja etsii arvonlisäveroryhmät, joilla on vastaavat kohteeseen perustuvat verokriteerit. Esimerkiksi online-tilauksessa, jonka rivinimikkeen toimitusosoite on San Francisco, Kalifornia, veromoduuli etsii arvonlisävero ryhmän ja arvonlisäverokoodin Kaliforniasta ja laskee sitten kunkin rivinimikkeen veron sen mukaisesti.  

## <a name="customer-based-tax-groups"></a>Asiakaspohjaiset veroryhmät

Commerce-pääkonttorisovelluksessa on kaksi paikkaa, joissa asiakkaan veroryhmät on konfiguroitu:

- **Asiakkaan profiili**
- **Asiakkaan toimitusosoite**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Jos asiakkaan profiilissa on määritetty veroryhmä

Asiakkaan profiilitietueeseen pääkonttorisovelluksessa voi olla määritetty arvonlisäveroryhmä, mutta online-tilauksissa veromoduuli ei käytä asiakkaan profiiliin konfiguroituja arvonlisäveroryhmiä. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Jos asiakkaan toimitusosoitteessa on määritetty veroryhmä

Jos asiakkaan toimitusosoitteen tietueessa on määritetty veroryhmä ja online-tilaus (tai rivinimike) toimitetaan asiakkaan toimitusosoitteeseen, veromoduuli käyttää asiakkaan osoitetietueeseen konfiguroituja veroryhmiä verolaskelmissa.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Veroryhmän määrittäminen asiakkaan toimitusosoitteen tietueessa

Voit määrittää asiakkaan toimitusosoitetietueen veroryhmän Commerce-pääkonttorisovelluksessa seuraavasti:

1. Siirry kohtaan **Kaikki asiakkaat** ja valitse haluamasi asiakas. 
1. Valitse **Osoitteet**-pikavälilehdessä haluamasi osoite ja valitse sitten **Lisää vaihtoehtoja \> Lisäasetukset**. 
1. Määritä arvonlisäveron arvo **Osoitteiden hallinta**-sivun **Yleiset**-välilehdessä.

> [!NOTE]
> Veroryhmä määritetään tilausrivin toimitusosoitteen avulla, ja kohteeseen perustuvat verot määritetään itse veroryhmässä. Lisätietoja on kohdassa [Määränpäähän perustuvien verojen määrittäminen online-myymälöille](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>Tilauksen nouto myymälästä

Jos tilausrivit on määritetty noudettaviksi myymälästä tai tien vierestä, valitun noutomyymälän veroryhmä otetaan käyttöön. Lisätietoja tietyn myymälän veroryhmän konfiguroinnista on kohdassa [Muiden veroasetusten määrittäminen myymälöille](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> Kun tilausrivi noudetaan myymälästä, veromoduuli ohittaa asiakkaan osoitteen veroasetukset (jos se on määritetty) ja noutomyymälän verokonfiguraatio otetaan käyttöön. 

## <a name="additional-resources"></a>Lisäresurssit

[Arvonlisäveron yleiskatsaus](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Arvonlisäveron laskentatavat Alkuperä-kentässä](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[Arvonlisäveron määrittäminen ja ohitukset](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Arvonlisäverokoodien koko summan ja välin laskentavaihtoehdot](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Verovapauden laskenta](tax-exempt-price-inclusive.md) 

