---
title: Asiakastilin maksutavan määrittäminen B2B-verkkokauppasivustoille
description: Tässä aiheessa kuvataan, kuinka asiakastilin maksutapa konfiguroidaan yritysten välisissä (B2B) verkkokauppasivustoissa.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 82dfd6ac7e97d838ef442fd6ded4a4f165fc795b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211198"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Asiakastilin maksutavan määrittäminen B2B-verkkokauppasivustoille

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka asiakastilin maksutapa konfiguroidaan yritysten välisissä (B2B) verkkokauppasivustoissa.

Vähittäismyyjät voivat hyväksyä useantyyppisiä maksutapoja verkkokauppakanavissaan myymistään tuotteista ja palveluista. Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä Microsoft Dynamics 365 Commercessa, kun järjestelmä määritetään. Asiakastilin (tai tilillä olevan) maksutavan on oltava tuettuna B2B-verkkokauppasivustoissa. 

## <a name="prerequisites"></a>Edellytykset

1. Lisää asiakastilin maksutapa Commerce headquarters -sovelluksessa.
2. Liitä asiakastilin maksutapa sähköistä kaupankäyntikanavaa varten.
3. Varmista, että **Salli ennakkomaksu** on käytössä asiakkaalle Commerce headquarters -sovelluksessa kohdassa **Retail ja Commerce \> Asiakkaat \> Kaikki asiakkaat \> Maksujen oletusasetukset**. Varmista myös, että **Luottoraja**-parametrit on määritetty oikein asiakkaalle Commerce headquarters -sovelluksen kohdassa **Retail ja Commerce \> Asiakkaat \> Kaikki asiakkaat \> Luotonvalvonta**. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Asiakastilin maksutavan ottaminen käyttöön Commercen sivustonmuodostimessa 

Saat asiakastilin maksutavan otettua käyttöön Commercen sivustonmuodostimessa seuraavasti.

1. Siirry kohtaan **Sivuston asetukset \> Laajennukset**.
1. Määritä **Ota käyttöön asiakastilin maksut** -ominaisuuden arvoksi **Käytössä B2B-asiakkaille**. 
1. Valitse **Tallenna ja julkaise**.

> [!NOTE]
> Uudet sivuston asetukset tulevat voimaan vasta, kun app.settings.json-tiedosto on päivitetty. Lisätietoja on ohjeaiheessa [SDK:n ja moduulikirjaston päivitykset](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Asiakastilin maksutavan ottaminen käyttöön B2B-verkkokauppasivuston uloskuittaussivulla

Saat asiakastilin maksutavan otettua käyttöön B2B-verkkokauppasivuston uloskuittaussivulla seuraavasti.

1. Etsi ja muokkaa Commercen sivustonmuodostintyökalussa uloskuittaussivu tai katkelmassa, joka sisältää B2B-verkkokauppasivuston uloskuittausmoduulin.
1. Valitse **Kassaosiokontti**-paikassa **Lisää moduuli** ja lisää sitten **Asiakastilin maksu** -moduuli.
1. Aseta **Asiakastilin maksu** -moduuli valitsemalla kolme pistettä (**...**) ja valitsemalla sitten **Siirrä ylös** tai **Siirrä alas** tarvittaessa.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Vahvista, että asiakastilin maksutapa on otettu käyttöön ja julkaistu

Voit vahvistaa, että asiakastilin maksutapa on otettu käyttöön ja julkaistu, seuraavasti.

1. Kirjaudu sisään verkkokauppasivustoon.
1. Lisää tuote ostoskoriin.
1. Siirry kassasivulle. Tässä pitäisi näkyä uusi **Asiakastili**-maksutapaa.

## <a name="additional-resources"></a>Lisäresurssit

[B2B-verkkokauppasivuston määrittäminen](set-up-b2b-site.md)

[Organisaation mallinnushierarkioiden luominen B2B-organisaatioille](org-model.md)

[Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa](manage-b2b-users.md)

[Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille](quantity-limits.md)

[SDK:n ja moduulikirjaston päivitykset](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]