---
title: Siirtotilausasiakirjojen verotietojen tulostaminen
description: Tässä aiheessa kuvataan, miten veronlaskentapalvelun määrittämät verotiedot voidaan tulostaa siirtotilausasiakirjoissa.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e74336270ab46fc19adb4c797745c9582028391a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687468"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Siirtotilausasiakirjojen verotietojen tulostaminen

[!include [banner](../../includes/banner.md)]

Tässä aiheessa selitetään, miten verotiedot tulostetaan siirtotilausasiakirjoissa. Voit tulostaa siirtotilauksen proformalaskun sellaisten varastosiirtojen osalta, jotka katsotaan yhteisöluovutuksiksi ja -hankinoiksi Euroopan unionin arvonlisäsäännösten mukaan. 

Seuraavat verojen kannalta merkitykselliset tiedot lisätään siirtotilausasiakirjoihin:

- Nimet ja lähetys- ja vastaanotto-osoitteet varastosiirtoa varten
- Toimittajan ja vastaanottajan verotunnisteet
- Toimitettujen tuotteiden yksikköhinta ja verotettava summa
- Verokoodi, veroprosentti, verosumma ja verodirektiivit

Näiden tietojen määrittämistä varten on suoritettava seuraavat päävaiheet.

1. [Siirtotilausten vero-ominaisuuden käyttöönotto ja määritys](tasks/Tax-feature-support-for-transfer-order.md).
2. [Useiden verorekisteröintinumeroiden luominen ja määrittäminen yritykselle ](emea-multiple-vat-registration-numbers.md).
3. Määritä vapauskoodi, kuvaus, verodirektiivit ja verokoodien tulostuskoodi. Tässä esimerkissä Microsoft Dynamics 365 Financessa luodaan ja synkronoidaan kolme verokoodia: **NL-Exempt**, **BE-RC-21** ja **BE-RC+21**.

    1. Valitse Financessa **Vero** \> **Asetukset** \> **Arvonlisävero** \> **Arvonlisäveron vapautuskoodit**.
    2. Valitse **Muokkaa** ja anna määritys **EY**-vapautuskoodille. Syötä esimerkiksi **Verovapaat EY-lähetykset ja verorekisteröintinumero**.
    3. Valitse **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäverokoodit**.
    4. Valitse verokoodi **BE-RC-21** ja sitten **Verodirektiivit**.
    5. Valitse **Uusi**.
    6. Valitse **Kieli**-kentässä **FI-FI**. Syötä sitten **Teksti**-kenttään **Asiakirja, jolla määritetään tuotteiden siirto EU:n arvonlisädirektiivin 2006/112/EY artiklan 138. 2. c) tarkoituksessa**.
    7. Sulje sivu.
    8. Valitse **Yleiset**-pikavälilehden **Tulosta**-kentässä **Arvonlisäveroprosentti**.
    8. Valitse **NL-Exempt**-verokoodi ja valitse sitten **Yleiset**-pikavälilehden **Tulosta**-kentässä **Arvonlisäprosentti**.

    > [!NOTE] 
    > Siirtotilausasiakirjoihin ei tulosteta verokoodia, veroprosenttia ja verovapauskuvausta, jos verokoodille ei ylläpidetä vapautuskoodin kuvausta tai verodirektiivejä.

## <a name="print-the-transfer-order---shipment-document"></a>Siirtotilauksen tulostus – lähetysasiakirja

Kun siirto on lähetetty, voit tulostaa siirtotilauksen lähetysasiakirjan seuraavasti.

1. Siirry kohtaan **Varastonhallinta** \> **Kyselyt ja raportit** \> **Siirtotilaukset** \> **Lähetys**.
2. Ota **Verotiedot** käyttöön **Tulosta**-ryhmän **Parametrit**-välilehdessä.
3. Valitse **Sisällytettävät tietueet**-välilehdessä **Suodatin**, valitse siirtotilauksen numero ja valitse sitten **OK**.
4. Tulosta siirtotilauksen lähetysasiakirja valitsemalla **OK**.

## <a name="print-the-transfer-order---receipt-document"></a>Siirtotilauksen tulostus – vastaanottoasiakirja

Kun siirto on otettu vastaan, voit tulostaa siirtotilauksen vastaanottoasiakirjan seuraavasti.

1. Siirry kohtaan **Varastonhallinta** \> **Kyselyt ja raportit** \> **Siirtotilaukset** \> **Vastaanotto**.
2. Ota **Verotiedot** käyttöön **Tulosta**-ryhmän **Parametrit**-välilehdessä.
3. Valitse **Sisällytettävät tietueet**-välilehdessä **Suodatin**, valitse siirtotilauksen numero ja valitse sitten **OK**.
4. Tulosta siirtotilauksen vastaanottoasiakirja valitsemalla **OK**.

## <a name="print-the-transfer-overview-document"></a>Siirron yhteenvetoasiakirjan tulostus

Noudattamalla näitä ohjeita voit tulostaa siirron yhteenvetoasiakirjan.

> [!NOTE]
> Verotiedot ovat käytettävissä vain, kun siirtotilaus on lähetetty tai vastaanotettu.

1. Siirry kohtaan **Varastonhallinta** \> **Kyselyt ja raportit** \> **Siirtotilaukset** \> **Siirron yhteenveto**.
2. Ota **Verotiedot** käyttöön **Tulosta**-ryhmän **Parametrit**-välilehdessä.
3. Valitse **Sisällytettävät tietueet**-välilehdessä **Suodatin**, valitse siirtotilauksen numero ja valitse sitten **OK**.
4. Tulosta siirtotilauksen yhteenvetoasiakirja valitsemalla **OK**.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
