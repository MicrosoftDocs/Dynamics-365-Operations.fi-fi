---
title: Tuotekonfiguraatioiden käyttäminen uudelleen
description: Voit määrittää, että haluat uudelleenkäyttää automaattisesti tuotteen aiemmin luotua konfiguraatiota. Kun käyttäjän määritysistunto on valmis, järjestelmä tarkistaa, onko käyttäjän valintoja vastaava konfiguraatio jo olemassa. Jos vastaava konfiguraatio löytyy, konfiguraatiotunnusta, vastaavaa tuoterakennetta ja reititystä käytetään uudelleen.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a3aca07388a440ce5168fa4106d90d931f7f194
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812784"
---
# <a name="reuse-product-configurations"></a><span data-ttu-id="6ed30-105">Tuotekonfiguraatioiden käyttäminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="6ed30-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ed30-106">Voit määrittää, että haluat uudelleenkäyttää automaattisesti tuotteen aiemmin luotua konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="6ed30-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="6ed30-107">Kun käyttäjän määritysistunto on valmis, järjestelmä tarkistaa, onko käyttäjän valintoja vastaava konfiguraatio jo olemassa.</span><span class="sxs-lookup"><span data-stu-id="6ed30-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="6ed30-108">Jos vastaava konfiguraatio löytyy, konfiguraatiotunnusta, vastaavaa tuoterakennetta ja reititystä käytetään uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6ed30-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="6ed30-109">Konfiguraatioiden uudelleenkäytön vaatimukset</span><span class="sxs-lookup"><span data-stu-id="6ed30-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="6ed30-110">Konfiguraatioiden uudelleenkäyttöä varten on määritettävä seuraavat komponenttien ja ominaisuuksien tiedot **Tuotemääritysmallin tietoja** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="6ed30-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="6ed30-111">**Komponentit ja alikomponentit** – Valitse **yleiset** pikavälilehden **Käytä konfiguraatioita** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6ed30-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="6ed30-112">**Määritteet** – Valitse **määritteet** pikavälilehdessä **Sisällytä uudelleenkäyttöön** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="6ed30-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="6ed30-113">Tämä vaihtoehto on käytettävissä vain, kun liittyvä komponentti on määritetty uudelleenkäyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="6ed30-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="6ed30-114">Jos et valitse mitään uudelleenkäytön määritteitä, konfiguraatiota käytetään aina uudelleen, riippumatta käyttäjän valinnoista määritysistunnon aikana.</span><span class="sxs-lookup"><span data-stu-id="6ed30-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="6ed30-115">Käytössä olevien konfiguraatioiden määritteiden arvojen  on vastattava käyttäjän valintoja,</span><span class="sxs-lookup"><span data-stu-id="6ed30-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="6ed30-116">Jos käyttäjä esimerkiksi valitsee **sininen** väriksi määritysistunnossa, järjestelmä tarkistaa, onko aiemmin luodun komponentin konfiguraatiossa sininen väri.</span><span class="sxs-lookup"><span data-stu-id="6ed30-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="6ed30-117">Konfiguraation uudelleenkäytön nollaaminen</span><span class="sxs-lookup"><span data-stu-id="6ed30-117">Resetting configuration reuse</span></span>
<span data-ttu-id="6ed30-118">Kun nollaat konfiguroinnin uudelleenkäytön, aiemmin luotuja konfiguraatioita ei enää käsitellä.</span><span class="sxs-lookup"><span data-stu-id="6ed30-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="6ed30-119">Voit halutessasi nollata konfiguroinnin uudelleenkäytön, jos tuoterakennetta tai reititystä on muutettu, mutta niihin liittyviä määritteitä ei ole muutettu.</span><span class="sxs-lookup"><span data-stu-id="6ed30-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="6ed30-120">Konfiguroinnin uudelleenkäyttö nollataan kohdassa **yleiset** komponentin pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="6ed30-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]