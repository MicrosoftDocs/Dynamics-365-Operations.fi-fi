---
title: Sähköisten asiakirjojen luominen ja päivittäminen sovellustiedoilla sähköistä raportointia (ER) käyttäen
description: Voit suunnitella sähköisen raportoinnin muotoja, joilla voidaan luoda sovelluksessa lähteviä sähköisiä asiakirjoja.
author: NickSelin
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 863c69446e9a7d447847483ec129788e85a8fd58
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750031"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="50aef-103">Sähköisten asiakirjojen luominen ja sovellustietojen päivittäminen ER:n avulla</span><span class="sxs-lookup"><span data-stu-id="50aef-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50aef-104">Voit suunnitella sähköisen raportoinnin muotoja, joilla voidaan luoda sovelluksessa lähteviä sähköisiä asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="50aef-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="50aef-105">Voit suunnitella myös sähköisiä raportointimuotoja, jotka jäsentävät saapuvia sähköisiä asiakirjoja ja jotka päivittävät sovelluksen tiedot kyseisten asiakirjojen tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="50aef-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="50aef-106">Tämän toiminnon avulla yhdellä sähköisen raportoinnin muodolla voidaan luoda lähteviä sähköisiä asiakirjoja ja päivittää sitten sovelluksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="50aef-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="50aef-107">Tätä toimintoa voidaan käyttää seuraavissa skenaarioissa:</span><span class="sxs-lookup"><span data-stu-id="50aef-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="50aef-108">Voit estää sovelluksen tietojen toistuvan käytön myöhemmissä prosessissa merkitsemällä sovelluksen tiedot heti, kun niillä on luotu sähköisiä asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="50aef-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="50aef-109">Voit esimerkiksi merkitä maksutapahtumat käsitellyiksi heti, kun ne on sisällytetty luotuun maksusanomaan.</span><span class="sxs-lookup"><span data-stu-id="50aef-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="50aef-110">Sähköisen raportoinnin logiikan avulla luotujen sähköisten asiakirjojen käsittelytietojen tallennus,</span><span class="sxs-lookup"><span data-stu-id="50aef-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="50aef-111">Esimerkiksi yksilöllinen maksusanoman tunnus, joka luodaan ER-lausekkeella.</span><span class="sxs-lookup"><span data-stu-id="50aef-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="50aef-112">Lauseke perustuu tietoihin, jotka annettiin ER-valintaikkunassa, kun asiakirjoja luodaan suorittamalla sähköisen raportoinnin muoto.</span><span class="sxs-lookup"><span data-stu-id="50aef-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="50aef-113">Saat lisätietoja tästä ominaisuudesta toistamalla joukon ER-luontiasiakirjoja sovellustietojen päivityksen tehtäväoppaassa (osa liiketoimintaprosessia 7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)), joka opastaa Intrastat-raportoinnin ja -arkistoinnin vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="50aef-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="50aef-114">Seuraavat tiedostot tarvitaan joidenkin tehtäväoppaiden vaiheiden suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="50aef-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="50aef-115">Lataa ja tallenna nämä tiedostot paikallisesti tietokoneeseen.</span><span class="sxs-lookup"><span data-stu-id="50aef-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="50aef-116">Sähköisen raportoinnin tietomallien määritys: Intrastat (malli)</span><span class="sxs-lookup"><span data-stu-id="50aef-116">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="50aef-117">Sähköisen raportoinnin mallin yhdistämismäärityksen määrittäminen: Intrastat (yhdistämismääritys)</span><span class="sxs-lookup"><span data-stu-id="50aef-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="50aef-118">Sähköisen raportointimuodon määritys: Intrastat (muoto)</span><span class="sxs-lookup"><span data-stu-id="50aef-118">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]