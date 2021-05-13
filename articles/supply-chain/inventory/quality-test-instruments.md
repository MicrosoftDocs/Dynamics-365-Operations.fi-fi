---
title: Laadunhallinnan testin mittavälineet
description: Tässä aiheessa kuvataan, kuinka luodaan testin mittavälineitä, joita voidaan käyttää laatutilausten testeissä Microsoft Dynamics 365 Supply Chain Managementissa.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc09021f89a9064a3140a726fca74e3eceab13da
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956640"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="7d70b-103">Laadunhallinnan testin mittavälineet</span><span class="sxs-lookup"><span data-stu-id="7d70b-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d70b-104">Tässä aiheessa kuvataan, kuinka luodaan testin mittavälineitä, joita voidaan käyttää laatutilausten testeissä Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="7d70b-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="7d70b-105">**Testin mittavälineet** -sivulla voit määrittää ja tarkastella tietoja laitteista, joita käytetään laatutilausten testien suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="7d70b-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="7d70b-106">Testin mittavälineet ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="7d70b-106">Test instruments are optional.</span></span> <span data-ttu-id="7d70b-107">Ne voivat kuitenkin auttaa laatutyöntekijöitä tietämään, mitä laitetta tai työkalua heidän tulee käyttää tietyn testin suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="7d70b-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="7d70b-108">Esimerkki testin mittavälineestä</span><span class="sxs-lookup"><span data-stu-id="7d70b-108">Test instrument example</span></span>

<span data-ttu-id="7d70b-109">Suoritat useita sähkökomponenttien testejä.</span><span class="sxs-lookup"><span data-stu-id="7d70b-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="7d70b-110">Jotkut testit koskevat komponenttien jännitelähtöä, yksi testi niiden lämpötilaa ja yksi testi niiden painoa.</span><span class="sxs-lookup"><span data-stu-id="7d70b-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="7d70b-111">Testien suorittamiseen käytetään erilaisia työkaluja, laitteita tai laitteistoja.</span><span class="sxs-lookup"><span data-stu-id="7d70b-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="7d70b-112">Esimerkiksi jännitemittaria käytetään jännitteen mittaamiseen, lämpömittaria lämpötilan mittaamiseen ja vaakaa painon mittaamiseen.</span><span class="sxs-lookup"><span data-stu-id="7d70b-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="7d70b-113">Voit konfiguroida kunkin näistä laitteista testin mittavälineenä ja määrittää mittayksikön, jolla testitulokset on kirjattava.</span><span class="sxs-lookup"><span data-stu-id="7d70b-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="7d70b-114">Esimerkiksi jännitemittarin tulokset tallennetaan voltteina, lämpömittarin tulokset kirjataan Fahrenheit-asteina tai Celsius-asteina ja vaa'an tulokset kirjataan paunoina tai kilogrammoina.</span><span class="sxs-lookup"><span data-stu-id="7d70b-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="7d70b-115">Uuden testin mittavälineen luominen</span><span class="sxs-lookup"><span data-stu-id="7d70b-115">Create a test instrument</span></span>

1. <span data-ttu-id="7d70b-116">Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testin mittavälineet**.</span><span class="sxs-lookup"><span data-stu-id="7d70b-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="7d70b-117">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7d70b-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="7d70b-118">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="7d70b-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7d70b-119">**Testin mittaväline** – Määritä testin mittavälineen yksilöivä tunnus tai nimi.</span><span class="sxs-lookup"><span data-stu-id="7d70b-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="7d70b-120">**Kuvaus** – Anna testin mittavälineen yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="7d70b-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="7d70b-121">**Yksikkö** – Valitse yksikkö, jossa mittaväline mittaa tuloksia.</span><span class="sxs-lookup"><span data-stu-id="7d70b-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="7d70b-122">**Tarkkuus**-kenttä määritetään automaattisesti valitsemaani yksikköön perustuen.</span><span class="sxs-lookup"><span data-stu-id="7d70b-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="7d70b-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7d70b-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d70b-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7d70b-124">Additional resources</span></span>

- [<span data-ttu-id="7d70b-125">Laadunhallinnan testi</span><span class="sxs-lookup"><span data-stu-id="7d70b-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="7d70b-126">Laadunhallinnan testiryhmät</span><span class="sxs-lookup"><span data-stu-id="7d70b-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]