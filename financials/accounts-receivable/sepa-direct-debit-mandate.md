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
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>Määritä SEPA-suoraveloituksen oletusarvot



Yhtenäisen euromaksualueen (SEPA) suoraveloituksen avulla velkoja voi hakea varoja asiakkaan pankkitililtä, edellyttäen, että asiakas on antanut velkojalle siihen allekirjoitetun valtakirjan. Asiakkaan allekirjoittama valtakirja antaa velkojalle valtuuden maksun hakemiseen ja ohjaa asiakkaan pankin maksamaan maksukehotuksen. Tässä ohjeaiheessa on järjestetty näyttää prosessin määrittäminen SEPA-suoraveloituksen toimeksiannoissa.

## <a name="prerequisites"></a>Edellytykset
Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.

| Luokka       | Edellytys                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Maa/alue | Yrityksen ensisijaisen osoitteen on oltava seuraavissa maissa tai seuraavilla alueilla: Alankomaat, Belgia, Espanja, Italia, Itävalta, Ranska tai Saksa. |

1. Määritä numerosarja Suoraveloitus toimeksiantojen Suoraveloitus jokainen toimeksianto on yksilöllinen numero. Luo **Numerosarjat**-sivulla suoraveloitusvaltakirjojen numerosarja. Voit käyttää tätä tunnistetta suoraveloitusvaltakirjajärjestelmän numerosarjan määrittämiseen **Myyntireskontran parametrit** -sivulla.

2. Määritä Myyntireskontran parametrit Suoraveloitus toimeksiantojen käyttöä varten **Myyntireskontran parametrit** Suoraveloitus toimeksiantojen parametrien määrittäminen-sivulla. Voit määrittää parametrit, edelleen **Suoraveloitus** -välilehdessä muuta kuin, että oletusparametrit. Sitten **Number sequences** -välilehden Päivitä **toimeksiannon Suoraveloitustunnus** -kentässä on numerosarja, jonka olet määrittänyt aiemmin.

3. Määritä maksutapa, Suoraveloitus määrätään, Suoraveloitus toimeksiantojen maksutapa on määritettävä. Voit käyttää tätä maksutapaa laskukyselyille, joiden perusteella suoraveloitusmaksut luodaan. Määritä maksutapa **Maksutavat**-sivulla. Suoraveloitusvaltakirjan maksutapaa määritettäessä on suoritettava seuraavat maksutavan lisämääritykset:

-   Valitse **Maksutyyppi**-kentässä **Sähköinen maksu**.
-   Valinnainen: Jos uskot kunkin asiakkaasi on useita määrätään, joka **aikana** -kenttään **laskun**. Lasku luodaan erilliset laskut, ja kunkin maksun käyttävät toimeksianto, joka määritetään laskun.
-   Voit luoda maksuja suoraveloitusvaltakirjojen avulla valitsemalla **Vaadi valtakirjaa**. **Vaadi valtakirjaa** -vaihtoehto on käytettävissä vain, jos valitset **Sähköinen maksu** **Maksutyyppi**-kentässä.

Katso myös [Suoraveloitus-yleistä](sepa-direct-debit-overview.md) 

