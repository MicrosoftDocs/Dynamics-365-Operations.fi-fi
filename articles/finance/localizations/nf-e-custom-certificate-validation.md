---
title: Mukautetun NF-e-varmenteen vahvistus
description: Tässä ohjeaiheessa on tietoja mukautetun NF-e-varmenteen käyttöönottamisesta ja käyttämisestä.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442703"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="8cd6b-103">Mukautetun NF-e-varmenteen vahvistus</span><span class="sxs-lookup"><span data-stu-id="8cd6b-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cd6b-104">Kun mukautetun NF-e-varmenteen tarkistusominaisuus otetaan käyttöön, mukautettu vahvistus sallii yhteyden muodostamisen verkkopalveluihin.</span><span class="sxs-lookup"><span data-stu-id="8cd6b-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="8cd6b-105">Tämä yhteys on pakollinen, jotta NF-e voidaan lähettää ja vastaanottaa SEFAZ-valtuutus.</span><span class="sxs-lookup"><span data-stu-id="8cd6b-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="8cd6b-106">Varmenteen V5 **Palvelimen todentamisen tarkoitus** -ominaisuuden myöntäjä on Brasilian varmenteiden päämyöntäjä.</span><span class="sxs-lookup"><span data-stu-id="8cd6b-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="8cd6b-107">Tämä ominaisuus on oletusarvoisesti poistettu käytöstä ja se on otettava manuaalisesti käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8cd6b-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="8cd6b-108">Joissain tilanteissa automaattinen varmennepäivitys voi poistaa tämän ominaisuuden pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="8cd6b-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="8cd6b-109">Tämä vaikuttaa TLS-yhteyteen, eikä se ole enää luotettu varmenne.</span><span class="sxs-lookup"><span data-stu-id="8cd6b-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="8cd6b-110">Se vaikuttaa myös mahdollisuuteen myöntää NF-e tuotantoympäristöissä Minas Geraisin (MG) ja Paranán (PR) osavaltioissa.</span><span class="sxs-lookup"><span data-stu-id="8cd6b-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="8cd6b-111">Tämä päivitys antaa vaihtoehtoisen varmenteen vahvistusratkaisun, jolla voi muodostaa turvallisen yhteyden.</span><span class="sxs-lookup"><span data-stu-id="8cd6b-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


