---
title: Yksityisten osoitteiden käyttöoikeudet käyttöoikeusroolin mukaan
description: Tässä artikkelissa kerrotaan, miten ratkaista ongelma, jossa asiakas ei voi käyttää yksityisiä osoitteita.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fbe0e8acc1b879e4d7982b33413236432f25f630
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418304"
---
# <a name="access-to-private-addresses-by-security-role"></a>Yksityisten osoitteiden käyttöoikeudet käyttöoikeusroolin mukaan

**Ongelma**

Kun asiakas tekee kaksoiskappaleen käyttöoikeusroolista ja kirjautuu tänä uutena roolia, asiakas ei näe yksityiseksi merkittyjä osoitteita.

**Tarkkuus**

Asiakas voi ratkaista ongelman noudattamalla käyttöoikeusroolin kaksoiskappaletta koskevia ohjeita.

1. Valitse **Organisaation hallinto \> Yleinen osoitekirja \> Yleisen osoitekirjan parametrit**.
2. Siirrä uusi käyttöoikeusrooli **Yksityisen sijainnin suojaus** -välilehdessä **Käytettävissä olevat roolit** -luettelosta **Valitut roolit** -luetteloon.
3. Valitse **Tallenna**.

![Yleisen osoitekirjan parametrit -sivu](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]