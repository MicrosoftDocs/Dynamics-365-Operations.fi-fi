---
title: Pikatuonti/-vienti
description: Pikatuonti- ja vientitoiminnon tarkoitus on vähentää tuonti- ja vientivaiheita.
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: 57d0ce9d483f4c849855e4247b4fd0fd067abb1b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565303"
---
# <a name="quick-import-export"></a><span data-ttu-id="db99c-103">Pikatuonti/-vienti</span><span class="sxs-lookup"><span data-stu-id="db99c-103">Quick import export</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db99c-104">Pikatuonti- ja vientitoiminnon tarkoitus on vähentää tuonti- ja vientivaiheita.</span><span class="sxs-lookup"><span data-stu-id="db99c-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="db99c-105">Pikatuonti- ja vientiomaisuus on lisätty, jotta käyttäjät voivat tuoda tai viedä yksinkertaisia, nopeasti suoritettavia töitä.</span><span class="sxs-lookup"><span data-stu-id="db99c-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="db99c-106">Ihannetapauksessa tätä ominaisuutta käytetään skenaarioissa, joissa tiedosto yhdistetään automaattisesti järjestelmään eikä käyttäjän tarvitse käyttää yhdistämisen lisäasetuksia tai luoda toistuvia tuonti- tai vientitöitä.</span><span class="sxs-lookup"><span data-stu-id="db99c-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

- <span data-ttu-id="db99c-107">Tämä ominaisuus tukee sekä käyttövalmiita että mukautettuja yksikköjä.</span><span class="sxs-lookup"><span data-stu-id="db99c-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
- <span data-ttu-id="db99c-108">Tuonti on mahdollista tiedostoista tai, jos käytät ODBC-tietolähdettä, voi määrittää tuonnin valitsemalla kyselyn.</span><span class="sxs-lookup"><span data-stu-id="db99c-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
- <span data-ttu-id="db99c-109">Sinulla on oltava aiemmin määritetyt AX- tai tiedostomuotoiset lähdetietomuodot ja sinun on tiedettävä niiden sijainti.</span><span class="sxs-lookup"><span data-stu-id="db99c-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
- <span data-ttu-id="db99c-110">Pikatuontia tai -vientiä varten ei tarvitse luoda käsittelyryhmää, sillä järjestelmä luo sen automaattisesti tuonti- tai vientityön suorittamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="db99c-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="db99c-111">Voit myös säilyttää halutessasi pikatuonnilla- tai viennillä tuotujen tietojen historiatiedot.</span><span class="sxs-lookup"><span data-stu-id="db99c-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="db99c-112">Huomaa, että pikatuonti- ja vientitoiminto olettaa, että tunnet DIXF-käsitteet.</span><span class="sxs-lookup"><span data-stu-id="db99c-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>





[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]