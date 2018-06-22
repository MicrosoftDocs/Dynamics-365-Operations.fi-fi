---
title: "Luotujen tiedostojen jakaminen tiedoston koon ja sisällön määrän perusteella"
description: "Tässä aiheessa on tietoja siitä, miten voit jakaa luodut tiedostot koon ja sisältönimikemäärän mukaan."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: afdf5b2596af7641182be50ced8159967164b115
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2018

---

# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="0f5e8-103">Luotujen XML-tiedostojen jakaminen tiedoston koon ja sisällön määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="0f5e8-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0f5e8-104">Voit suunnitella sähköisen raportoinnin (ER) muotoja luodaksesi lähteviä tiedostoja XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="0f5e8-105">Joskus nämä asiakirjat voidaan hyväksyä vain, kun ne täyttävät tietyt ehdot, kuten tiedoston enimmäiskoko tai joidenkin XML-solmujen enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="0f5e8-106">Voit suunnitella ER-muotoja luodaksesi sähköisiä asiakirjoja, jotka täyttävät tiedostojen vastaanottajien vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="0f5e8-107">FILE-muotoelementille voit määrittää tiedostokoon rajoituksen ER-lausekkeena.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="0f5e8-108">Jos määritetty raja ylittyy ER-raporttia luotaessa, ER viimeistelee nykyisen tiedoston luonnin ja siirtyy sitten seuraavan tiedoston luomiseen.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="0f5e8-109">Kaikille XML ELEMENT -muodoille voit määrittää elementtien määrän rajoituksen ER-lausekkeena.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="0f5e8-110">Jos luotavan tiedoston XML-solmujen määritetty raja ylittyy ER-raporttia suoritettaessa, ER viimeistelee nykyisen tiedoston luonnin ja siirtyy sitten seuraavan tiedoston luomiseen.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="0f5e8-111">Kaikille XML SEQUENCE -muotoelementeille voit määrittää alielementtien määrän rajoituksen ER-lausekkeena.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="0f5e8-112">Jos luotavan tiedoston muotoelementin sisäkkäisten XML-solmujen määritetty raja ylittyy ER-raporttia suoritettaessa, ER viimeistelee nykyisen tiedoston luonnin ja siirtyy sitten seuraavan tiedoston luomiseen.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="0f5e8-113">Voit merkitä minkä tahansa XML ELEMENT muotoelementin katkeamattomaksi.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="0f5e8-114">Näin voit säilyttää sisäkkäiset nimikkeet XML-solmuille, jotka on luodaan muotoelementin alle yhdessä muodostetussa tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="0f5e8-115">XML ELEMENT- ja XML SEQUENCE -muotoelementtien lisäksi voit lisätä XML-solmuja luotavaan tiedostoon myös RAW XML -muotoelementin avulla.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="0f5e8-116">Kuitenkaan solmuja, jotka lisäät RAW XML -muotoelementin avulla, ei oteta huomioon laskettaessa solmujen määrää, kun arvioidaan elementtien määrien rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="0f5e8-117">Jos olet määrittänyt tiedostokohteita FILE-muotoelementille, joka on määritetty jakamaan luodun tuloksen aina, kun tietyt rajat ylittyvät, muodostetun tuloksen kukin osa lähetetään määritettyyn tiedostokohteeseen yksittäisenä tiedostona.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="0f5e8-118">Jotta voisit nimetä tulostetta jakamalla luodut tiedostot yksilöllisesti, sinun on määritettävä ER-lauseke FILE-muotoelementille.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="0f5e8-119">Jos lisäät NUMBER SEQUENCE -tyypin ER-tietolähteen, numerosarjaa kasvatetaan kullekin tuloksen jaon osalle.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="0f5e8-120">Lisätietoja tästä toiminnosta saat toistamalla tehtäväoppaan **ER – XML-tiedostojen jakaminen tiedoston koon tai sisältökohteiden määrän perusteella**, joka on osa **7.5.4.3 Hanki/Kehitä IT-palvelu/ratkaisukomponentit (10677)** -liiketoimintaprosessia, jonka voi ladata [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="0f5e8-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="0f5e8-121">Tässä tehtäväoppaassa näet, miten voit määrittää ER-muodon jakamaan luotavat tiedostot rajoitusten koon ja sisällön nimikemäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="0f5e8-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="0f5e8-122">Lataa seuraavat tiedostot suorittaaksesi tehtäväoppaan:</span><span class="sxs-lookup"><span data-stu-id="0f5e8-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="0f5e8-123">ER-mallin määritys - XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="0f5e8-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="0f5e8-124">ER-muodon määritys - XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="0f5e8-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a><span data-ttu-id="0f5e8-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0f5e8-125">Additional resources</span></span>
[<span data-ttu-id="0f5e8-126">Sähköisen raportoinnin kohteet</span><span class="sxs-lookup"><span data-stu-id="0f5e8-126">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="0f5e8-127">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="0f5e8-127">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)


