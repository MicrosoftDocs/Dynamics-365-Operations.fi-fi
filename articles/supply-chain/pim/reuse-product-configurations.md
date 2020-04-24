---
title: Tuotekonfiguraatioiden käyttäminen uudelleen
description: Voit määrittää, että haluat uudelleenkäyttää automaattisesti tuotteen aiemmin luotua konfiguraatiota. Kun käyttäjän määritysistunto on valmis, järjestelmä tarkistaa, onko käyttäjän valintoja vastaava konfiguraatio jo olemassa. Jos vastaava konfiguraatio löytyy, konfiguraatiotunnusta, vastaavaa tuoterakennetta ja reititystä käytetään uudelleen.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f72d93600db3d9bf0a44ac1fe84111527bb31d0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209396"
---
# <a name="reuse-product-configurations"></a><span data-ttu-id="2b81a-105">Tuotekonfiguraatioiden käyttäminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="2b81a-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b81a-106">Voit määrittää, että haluat uudelleenkäyttää automaattisesti tuotteen aiemmin luotua konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="2b81a-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="2b81a-107">Kun käyttäjän määritysistunto on valmis, järjestelmä tarkistaa, onko käyttäjän valintoja vastaava konfiguraatio jo olemassa.</span><span class="sxs-lookup"><span data-stu-id="2b81a-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="2b81a-108">Jos vastaava konfiguraatio löytyy, konfiguraatiotunnusta, vastaavaa tuoterakennetta ja reititystä käytetään uudelleen.</span><span class="sxs-lookup"><span data-stu-id="2b81a-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="2b81a-109">Konfiguraatioiden uudelleenkäytön vaatimukset</span><span class="sxs-lookup"><span data-stu-id="2b81a-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="2b81a-110">Konfiguraatioiden uudelleenkäyttöä varten on määritettävä seuraavat komponenttien ja ominaisuuksien tiedot **Tuotemääritysmallin tietoja** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="2b81a-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="2b81a-111">**Komponentit ja alikomponentit** – Valitse **yleiset** pikavälilehden **Käytä konfiguraatioita** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2b81a-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="2b81a-112">**Määritteet** – Valitse **määritteet** pikavälilehdessä **Sisällytä uudelleenkäyttöön** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2b81a-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="2b81a-113">Tämä vaihtoehto on käytettävissä vain, kun liittyvä komponentti on määritetty uudelleenkäyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="2b81a-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="2b81a-114">Jos et valitse mitään uudelleenkäytön määritteitä, konfiguraatiota käytetään aina uudelleen, riippumatta käyttäjän valinnoista määritysistunnon aikana.</span><span class="sxs-lookup"><span data-stu-id="2b81a-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="2b81a-115">Käytössä olevien konfiguraatioiden määritteiden arvojen  on vastattava käyttäjän valintoja,</span><span class="sxs-lookup"><span data-stu-id="2b81a-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="2b81a-116">Jos käyttäjä esimerkiksi valitsee **sininen** väriksi määritysistunnossa, järjestelmä tarkistaa, onko aiemmin luodun komponentin konfiguraatiossa sininen väri.</span><span class="sxs-lookup"><span data-stu-id="2b81a-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="2b81a-117">Konfiguraation uudelleenkäytön nollaaminen</span><span class="sxs-lookup"><span data-stu-id="2b81a-117">Resetting configuration reuse</span></span>
<span data-ttu-id="2b81a-118">Kun nollaat konfiguroinnin uudelleenkäytön, aiemmin luotuja konfiguraatioita ei enää käsitellä.</span><span class="sxs-lookup"><span data-stu-id="2b81a-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="2b81a-119">Voit halutessasi nollata konfiguroinnin uudelleenkäytön, jos tuoterakennetta tai reititystä on muutettu, mutta niihin liittyviä määritteitä ei ole muutettu.</span><span class="sxs-lookup"><span data-stu-id="2b81a-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="2b81a-120">Konfiguroinnin uudelleenkäyttö nollataan kohdassa **yleiset** komponentin pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="2b81a-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>



