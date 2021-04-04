---
title: Sähköisen kaupan kehitysympäristön määrittäminen Tier 1 Retail Server -näennäiskoneen virheenkorjausta varten
description: Tässä aiheessa on ohjeet sähköisen kaupan kehitysympäristön määrittämiseksi Tier 1 Retail Server -näennäiskoneen (VM) virheenkorjausta varten.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35380a559a4f1b22bdf04ff25cb2bbfc51aff45b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585294"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>Sähköisen kaupan kehitysympäristön määrittäminen Tier 1 Retail Server -näennäiskoneen virheenkorjausta varten

[!include [banner](../../includes/banner.md)]

Tässä aiheessa on ohjeet sähköisen kaupan kehitysympäristön määrittämiseksi Tier 1 Retail Server -näennäiskoneen (VM) virheenkorjausta varten.

## <a name="description"></a>kuvaus

Microsoft Dynamics 365 Commerce Tier 1 -ympäristöt otetaan yleensä käyttöön Commerce Runtimen (CRT) ja myyntipisteen (POS) laajennusten kehitystyössä. Ne ovat itsenäisiä ympäristöjä. Ohjelmisto ei sisällä sähköisen kaupankäynnin komponentteja, koska arkkitehtuuri tarjoataan ohjelmisto palveluna (SaaS) -tyyppisesti.

Joissain tilanteissa kannattaa testata laajennuksia Tier 1 -ympäristössä, jotta voit tehdä virheenkorjausta laajennuksille sähköisen kaupan komponenteista. Yleiset ohjeet: [Virheenkorjaus tason 1 Commerce-kehitysympäristössä](../e-commerce-extensibility/debug-tier-1.md).

Kun teet virheenkorjausta Tier 1 -ympäristössä, koska sivusto kutsuu nyt eri Retail Server -palvelinta, palvelintenväliset kutsut voivat aiheuttaa erilaisia sisällön suojauskäytäntöön liittyviä virheitä.

Seuraavassa kuvassa on esimerkki virheestä, joka voi ilmetä, kun variantti valitaan tuotteen tietosivulla.

![Virhe, kun variantti valitaan tuotteen tiedot -sivulla](media/unhandled-rejection-error.jpg)

Seuraavassa kuvassa on esimerkki samanlaisesta virheestä selaimen virheenkorjaustyökaluissa (F12 Developer Tools). Virhesanomassa mainitaan sisällön suojauskäytännön direktiivin rike.

![Virheenkorjaustyökalujen virhe](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Ratkaisu

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Sivuston sisällön suojauskäytännön poistaminen käytöstä Commercen sivuston muodostintyökalussa

1. Valitse sivusto, jota käsittelet.
1. Valitse **Asetukset** ja valitse sitten **Laajennukset**.
1. Valitse **Sisällön suojauskäytäntö** -välilehdestä **Poista sisällön suojauskäytäntö käytöstä**.
1. Valitse **Tallenna ja julkaise**.

> [!NOTE]
> Yritysten ja kuluttajien välinen (B2C) kirjautuminen ei toimi paikallisessa kehitysympäristössä. Voit kuitenkin simuloida vierailijan kirjautumisen tai luoda näytesivuja simuloidaksesi käyttäjien kirjautumista tarpeen mukaan.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen kaupankäynnin online-laajennusten kehittämisen aloittaminen](../e-commerce-extensibility/sdk-getting-started.md)

[Sisällön suojauskäytännön (CSP) hallinta sähköisen kaupankäynnin sivustossa](../manage-csp.md)
