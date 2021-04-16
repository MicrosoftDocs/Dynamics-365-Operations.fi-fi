---
title: Ennalta ehkäisevä huolto – yleiskatsaus
description: Tässä ohjeaiheessa käsitellään käyttöomaisuuden hallinnan ennaltaehkäisevää ylläpitoa.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 15478776e9a2152b93e4413105145f2a40cdc506
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821654"
---
# <a name="preventive-maintenance-overview"></a><span data-ttu-id="e6a0f-103">Ennalta ehkäisevä huolto – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e6a0f-103">Preventive maintenance overview</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e6a0f-104">Tässä ohjeaiheessa käsitellään käyttöomaisuuden hallinnan ennaltaehkäisevää ylläpitoa.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-104">This topic explains preventive maintenance in Asset Management.</span></span> <span data-ttu-id="e6a0f-105">Ennaltaehkäisevä huolto on toimintaa, johon sisältyy suunniteltuja huoltotöitä, esimerkiksi säännöllistä huoltoa, kalibrointia ja tarkastuksia.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-105">Preventive maintenance is a discipline involving planned maintenance jobs, for example, regular service, calibration, and inspections.</span></span> <span data-ttu-id="e6a0f-106">**Resurssien hallinnassa** voit luoda ylläpitosuunnitelmia ja määrittää niitä resursseihin ja toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-106">In **Asset Management**, you can create maintenance plans and set them up on assets and functional locations.</span></span> <span data-ttu-id="e6a0f-107">Voit myös määrittää kunnossapitokierroksia toiminnallisille sijainneille.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-107">You can also set up maintenance rounds on functional locations.</span></span> <span data-ttu-id="e6a0f-108">Käyttöomaisuuserien ylläpitosuunnitelmat ovat aktiivisia riippumatta siitä, mihin omaisuuserä on asennettu.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-108">Maintenance plans on assets are active regardless of where the asset is installed.</span></span> <span data-ttu-id="e6a0f-109">Huoltosuunnitelmat ja kunnossapitokierrokset toiminnallisessa sijainnissa ovat aktiivisia sijainnissa tällä hetkellä asennetuille käyttöomaisuuksille.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-109">Maintenance plans and maintenance rounds on functional location are active for the assets currently installed at the location.</span></span> <span data-ttu-id="e6a0f-110">Sen sijaan, että määrittäisit käyttöomaisuuksien ylläpitosuunnitelmia tai määrittäisit ylläpitokierroksia toiminnallisissa sijainneissa, voit luoda kunnossapitokierroksia, joissa on useita käyttökohteita, joihin sinun on suoritettava samaan työrutiiniin liittyviä kunnossapitotöitä.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-110">Instead of setting up maintenance plans on assets, or setting up maintenance rounds on functional locations, you can create maintenance rounds that include multiple assets on which you need to perform related types of maintenance jobs in the same work routine.</span></span> <span data-ttu-id="e6a0f-111">Käyttökohteista luodut ylläpitokierrokset – sen sijaa että ne luotaisiin toiminnallisissa sijainneissa – tarkoittavat, että voit valita yhteen kunnossapitokierrokseen useita käyttöomaisuuksia, joita ei ole asennettu samaan toimintosijaintiin.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-111">Maintenance rounds created from assets - instead of created on functional locations - means that you can select a number of assets for one maintenance round, which are not installed on the same functional location.</span></span>

<span data-ttu-id="e6a0f-112">Huoltosuunnitelmia käytetään yksittäisten käyttöomaisuuksien ennaltaehkäisevään ja reaktiiviseen ylläpitoon.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-112">Maintenance plans are used for preventive and reactive maintenance on individual assets.</span></span> <span data-ttu-id="e6a0f-113">Kunnossapitokierroksia käytetään käyttöomaisuuseräjoukon tai -ryhmän ennaltaehkäisevään ylläpitoon.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-113">Maintenance rounds are used for preventive maintenance on a group or a set of assets.</span></span> <span data-ttu-id="e6a0f-114">Huoltosuunnitelmia ja kunnossapitokierroksia käytetään työtilausehdotusten luonnissa.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-114">Maintenance plans and maintenance rounds are used for generating work order proposals.</span></span> <span data-ttu-id="e6a0f-115">Työtilausehdotukset tallennetaan ylläpitoaikataulun riveinä, jotka voidaan niputtaa ja muuntaa työtilauksiksi.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-115">The work order proposals are saved as maintenance schedule lines, which can be bundled and converted into work orders.</span></span>

<span data-ttu-id="e6a0f-116">Alla olevassa kuvassa on yleiskatsaus työnkulkuun huoltosuunnitelmien ja kunnossapitokierrosten luomisesta käyttöomaisuuksien työtilausten luontiin näiden huoltosuunnitelmien ja kunnossapitokierrosten perusteella.</span><span class="sxs-lookup"><span data-stu-id="e6a0f-116">The following illustration provides an overview of the work flow from creating maintenance plans and maintenance rounds to creating work orders for assets, based on those maintenance plans and maintenance rounds.</span></span>

![Kuva 1](media/01-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]