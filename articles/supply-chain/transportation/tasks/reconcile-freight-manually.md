--- 
title: "Täsmäytä rahti manuaalisesti"
description: "Tässä menettelyssä kuvataan, miten rahti täsmäytetään manuaalisesti."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 28de4c720cd771f476f379d925e9500e41482aa6
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="reconcile-freight-manually"></a>Täsmäytä rahti manuaalisesti

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, miten rahti täsmäytetään manuaalisesti. Kuljetuskoordinaattori tekee tämän yleensä. Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.


## <a name="select-a-load-to-reconcile"></a>Valitse täsmäytettävä kuorma
1. Valitse Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila.
2. Poista Piilota toimitettu ja vastaanotettu -valintaruudun valinta. 
3. Valitse luettelossa kuorma, jonka tunnus on 00006.

## <a name="create-a-carrier-invoice"></a>Luo kuljettajan lasku
    * Jos rahti täsmäytetään manuaalisesti ja et vastaanota kuljettajan laskuja automaattisesti, voit luoda laskun rahtilaskun perusteella.  
1. Valitse Aiheeseen liittyviä tietoja.
2. Valitse Rahtilaskun tiedot.
3. Valitse Luo rahtilasku.
4. Kirjoita Lasku-kenttään arvo.
5. Valitse OK.

## <a name="reconcile-the-invoice"></a>Täsmäytä lasku
    * Kuljettajan lasku ja rahtilasku täsmäytetään rivi kerrallaan.  
1. Valitse Täsmäytä rahtilaskut ja laskut.
2. Laajenna Laskun tiedot -osa.
3. Laajenna Täsmäyttämättömän rahtilaskun tiedot -osa.
4. Merkitse valittu rivi luettelossa.
5. Valitse Täsmäytä.
6. Laajenna Täsmäytetyn rahtilaskun tiedot -osa.

## <a name="submit-the-invoice-for-approval"></a>Lähetä lasku hyväksyttäväksi
1. Valitse Lähetä hyväksyttäväksi.
2. Sulje sivu.
3. Poista Piilota hyväksytyt -valintaruudun valinta. 
4. Valitse Toimittajan laskun kirjauskansiot.
5. Avaa Viitekirjauskansion numero -kentän linkki napsauttamalla.
6. Valitse Rivit.

