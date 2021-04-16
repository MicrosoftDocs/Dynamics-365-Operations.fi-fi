---
title: Taloushallinnon dimensiot ja päätilit oikealta vasemmalle kirjoitettavilla kielillä
description: Tässä aiheessa käsitellään päätöksiä, joita on tehtävä käytettäessä oikealta vasemmalle kirjoitettavia kieliä, ja kun taloushallinnon dimensioita ja päätilin asetuksia on määritettävä.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 508f4ed4de367770acddc77a6ff5e7e36fd20729
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748134"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="a9bd5-103">Taloushallinnon dimensiot ja päätilit oikealta vasemmalle kirjoitettavilla kielillä</span><span class="sxs-lookup"><span data-stu-id="a9bd5-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9bd5-104">Tässä ohjeaiheessa käsitellään käyttöönottopäätöksiä, jotka koskevat oikealta vasemmalle kirjoitettavien kielien käyttöä määritettäessä taloushallinnon dimensioiden ja päätilin asetuksia.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="a9bd5-105">Taloushallinnon dimensiot ja päätilit ovat tärkeimmät käyttöönoton suunnitteluvaiheen komponentit.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="a9bd5-106">Kun taloushallinnon dimensiot ja päätilit on luotu järjestelmään, niitä käytetään **Määritä tilirakenteet**, **Lisäsäännön rakenteet** ja **Integrointisovellusten taloushallinnon dimension määritykset** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="a9bd5-107">Näillä sivuilla määritettyä tilausta käytetään järjestelmässä tietojen antamiseen ja kulutuksen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="a9bd5-108">Joissakin järjestelmän osissa taloushallinnan dimensiot ja päätilit näkyvät eri kentissä.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="a9bd5-109">Muualla, kuten kirjauskansioissa, taloushallinnon dimensiot ja päätilit näkyvät kuitenkin yhtenä merkkijonona.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-109">In other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="a9bd5-110">Parhaat käytännöt taloushallinnon dimensioiden ja päätilien määrittämiseen järjestelmässä oikealta vasemmalle kirjoitettavan kielellä</span><span class="sxs-lookup"><span data-stu-id="a9bd5-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

- <span data-ttu-id="a9bd5-111">Kun valitset tilikartan erotinta, valitse jokin kahden erottimen yhdistelmistä: kaksi peräkkäistä yhdysmerkkiä (`--`), kaksi pystyviivaa (`||`), kaksi peräkkäistä pilkkua (`..`) tai kaksi peräkkäistä alaviivaa (`\\`).</span><span class="sxs-lookup"><span data-stu-id="a9bd5-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (`--`), double bar (`||`), double period (`..`), or double underscore (`\\`).</span></span>
- <span data-ttu-id="a9bd5-112">Kun luot taloushallinnon dimension ja päätilin arvoja, käytä ainoastaan numeroita ja oikealta vasemmalle kirjoitettavan kielen merkkejä.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
- <span data-ttu-id="a9bd5-113">Älä käytä valitun tilikartan erotin kirjanpitodimension ja päätilin arvoina.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="a9bd5-114">Näitä toimintaohjeita noudattamalla autat takaamaan, että käyttäjän määrittämä järjestys on yhdenmukainen koko järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]