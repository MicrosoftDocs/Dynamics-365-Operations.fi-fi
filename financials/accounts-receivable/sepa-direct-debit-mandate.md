---
title: "Määritä SEPA-suoraveloituksen oletusarvot"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8cc0a11109fe5521586ea8abd7c0b97dce2c1591
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>Määritä SEPA-suoraveloituksen oletusarvot

[!include[banner](../includes/banner.md)]




Yhtenäisen euromaksualueen (SEPA) suoraveloituksen avulla velkoja voi hakea varoja asiakkaan pankkitililtä, edellyttäen, että asiakas on antanut velkojalle siihen allekirjoitetun valtakirjan. Asiakkaan allekirjoittama valtakirja antaa velkojalle valtuuden maksun hakemiseen ja ohjaa asiakkaan pankin maksamaan maksukehotuksen. Tässä ohjeaiheessa kuvataan SEPA-suoraveloitusvaltakirjojen määrittämisprosessi.

## <a name="prerequisites"></a>Edellytykset
Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.

| Luokka       | Edellytys                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Maa/alue | Yrityksen ensisijaisen osoitteen on oltava seuraavissa maissa tai seuraavilla alueilla: Alankomaat, Belgia, Espanja, Italia, Itävalta, Ranska tai Saksa. |

1. Määritä numerosarja suoraveloitusvaltakirjoille Jokaisella suoraveloitusvaltakirjalla on oltava yksilöllinen numero. Luo **Numerosarjat**-sivulla suoraveloitusvaltakirjojen numerosarja. Voit käyttää tätä tunnistetta suoraveloitusvaltakirjajärjestelmän numerosarjan määrittämiseen **Myyntireskontran parametrit** -sivulla.

2. Määritä suoraveloitusvaltakirjojen myyntireskontran parametrit Määritä **Myyntireskontran parametrit** -sivulla suoraveloitusvaltakirjan parametrit. Voit määrittää parametrit **Suoraveloitus**-välilehdellä muuttamalla oletusparametreja tarpeen mukaan. Päivitä sitten **Numerosarjat**-välilehden **Suoraveloitusvaltakirjan tunnus** -kenttään aiemmin määrittämäsi numerosarja.

3. Määritä maksutapa suoraveloitusvaltakirjoille Sinun on määritettävä maksutapa suoraveloitusvaltakirjoille. Voit käyttää tätä maksutapaa laskukyselyille, joiden perusteella suoraveloitusmaksut luodaan. Määritä maksutapa **Maksutavat**-sivulla. Suoraveloitusvaltakirjan maksutapaa määritettäessä on suoritettava seuraavat maksutavan lisämääritykset:

-   Valitse **Maksutyyppi**-kentässä **Sähköinen maksu**.
-   Valinnainen: Jos haluat, että asiakkailla on oltava useita valtuutuksia, valitse **Kausi**-kentässä **Lasku**. Ohjelma luo kullekin laskulle erillisen maksun, ja jokainen maksu käyttää laskulle määritettyä valtakirjaa.
-   Voit luoda maksuja suoraveloitusvaltakirjojen avulla valitsemalla **Vaadi valtakirjaa**. **Vaadi valtakirjaa** -vaihtoehto on käytettävissä vain, jos valitset **Sähköinen maksu** **Maksutyyppi**-kentässä.

Katso myös [Suoraveloitusyhteenveto](sepa-direct-debit-overview.md) 



