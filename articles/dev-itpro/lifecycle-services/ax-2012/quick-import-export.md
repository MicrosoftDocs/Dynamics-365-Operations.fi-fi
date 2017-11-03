---
title: "Pikatuonnin tai -viennin käyttäminen"
description: "Pikatuonti- ja vientitoiminnon tarkoitus on vähentää tuonti- ja vientivaiheita."
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: AX 2012
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 14b4a56a229a2e1eb15c29eb7a89a89ac31e58db
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a><span data-ttu-id="3660a-103">Test Data Transfer Tool (beta-versio) -sovelluksen ajaminen Dynamics AX:ssä (AX 2012)</span><span class="sxs-lookup"><span data-stu-id="3660a-103">Run the Test Data Transfer Tool (beta) for Dynamics AX (AX 2012)</span></span>

[!include[banner](../../includes/banner.md)]


<span data-ttu-id="3660a-104">Pikatuonti- ja vientitoiminnon tarkoitus on vähentää tuonti- ja vientivaiheita.</span><span class="sxs-lookup"><span data-stu-id="3660a-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="3660a-105">Pikatuonti- ja vientiomaisuus on lisätty, jotta käyttäjät voivat tuoda tai viedä yksinkertaisia, nopeasti suoritettavia töitä.</span><span class="sxs-lookup"><span data-stu-id="3660a-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="3660a-106">Ihannetapauksessa tätä ominaisuutta käytetään skenaarioissa, joissa tiedosto yhdistetään automaattisesti järjestelmään eikä käyttäjän tarvitse käyttää yhdistämisen lisäasetuksia tai luoda toistuvia tuonti- tai vientitöitä.</span><span class="sxs-lookup"><span data-stu-id="3660a-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

-   <span data-ttu-id="3660a-107">Tämä ominaisuus tukee sekä käyttövalmiita että mukautettuja yksikköjä.</span><span class="sxs-lookup"><span data-stu-id="3660a-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
-   <span data-ttu-id="3660a-108">Tuonti on mahdollista tiedostoista tai, jos käytät ODBC-tietolähdettä, voi määrittää tuonnin valitsemalla kyselyn.</span><span class="sxs-lookup"><span data-stu-id="3660a-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
-   <span data-ttu-id="3660a-109">Sinulla on oltava aiemmin määritetyt AX- tai tiedostomuotoiset lähdetietomuodot ja sinun on tiedettävä niiden sijainti.</span><span class="sxs-lookup"><span data-stu-id="3660a-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
-   <span data-ttu-id="3660a-110">Pikatuontia tai -vientiä varten ei tarvitse luoda käsittelyryhmää, sillä järjestelmä luo sen automaattisesti tuonti- tai vientityön suorittamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="3660a-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="3660a-111">Voit myös säilyttää halutessasi pikatuonnilla- tai viennillä tuotujen tietojen historiatiedot.</span><span class="sxs-lookup"><span data-stu-id="3660a-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="3660a-112">Huomaa, että pikatuonti- ja vientitoiminto olettaa, että tunnet DIXF-käsitteet.</span><span class="sxs-lookup"><span data-stu-id="3660a-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>




