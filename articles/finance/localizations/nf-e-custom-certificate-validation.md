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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f13e8b8229bbd9e174e5bde7858a468048ba309b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990083"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="3b473-103">Mukautetun NF-e-varmenteen vahvistus</span><span class="sxs-lookup"><span data-stu-id="3b473-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b473-104">Kun mukautetun NF-e-varmenteen tarkistusominaisuus otetaan käyttöön, mukautettu vahvistus sallii yhteyden muodostamisen verkkopalveluihin.</span><span class="sxs-lookup"><span data-stu-id="3b473-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="3b473-105">Tämä yhteys on pakollinen, jotta NF-e voidaan lähettää ja vastaanottaa SEFAZ-valtuutus.</span><span class="sxs-lookup"><span data-stu-id="3b473-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="3b473-106">Varmenteen V5 **Palvelimen todentamisen tarkoitus** -ominaisuuden myöntäjä on Brasilian varmenteiden päämyöntäjä.</span><span class="sxs-lookup"><span data-stu-id="3b473-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="3b473-107">Tämä ominaisuus on oletusarvoisesti poistettu käytöstä ja se on otettava manuaalisesti käyttöön.</span><span class="sxs-lookup"><span data-stu-id="3b473-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="3b473-108">Joissain tilanteissa automaattinen varmennepäivitys voi poistaa tämän ominaisuuden pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="3b473-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="3b473-109">Tämä vaikuttaa TLS-yhteyteen, eikä se ole enää luotettu varmenne.</span><span class="sxs-lookup"><span data-stu-id="3b473-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="3b473-110">Se vaikuttaa myös mahdollisuuteen myöntää NF-e tuotantoympäristöissä Minas Geraisin (MG) ja Paranán (PR) osavaltioissa.</span><span class="sxs-lookup"><span data-stu-id="3b473-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="3b473-111">Tämä päivitys antaa vaihtoehtoisen varmenteen vahvistusratkaisun, jolla voi muodostaa turvallisen yhteyden.</span><span class="sxs-lookup"><span data-stu-id="3b473-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


