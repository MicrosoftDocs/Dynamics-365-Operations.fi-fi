---
title: SEPA (Single Euro Payments Area) -suoraveloitusvaltakirjan asetukset
description: Yhtenäisen euromaksualueen (SEPA) suoraveloituksen avulla velkoja voi hakea varoja asiakkaan pankkitililtä, edellyttäen, että asiakas on antanut velkojalle siihen allekirjoitetun valtakirjan.
author: ShivamPandey-msft
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bea974750a6ac62d8ddeea5d9d4457f4846cb79
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891635"
---
# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA (Single Euro Payments Area) -suoraveloitusvaltakirjan asetukset

[!include [banner](../includes/banner.md)]

Yhtenäisen euromaksualueen (SEPA) suoraveloituksen avulla velkoja voi hakea varoja asiakkaan pankkitililtä, edellyttäen, että asiakas on antanut velkojalle siihen allekirjoitetun valtakirjan. Asiakkaan allekirjoittama valtakirja antaa velkojalle valtuuden maksun hakemiseen ja ohjaa asiakkaan pankin maksamaan maksukehotuksen. Tässä artikkelissa kuvataan SEPA-suoraveloitusvaltakirjojen määrittämisprosessi.

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

Lisäresurssit

[SEPA (Single Euro Payments Area) -suoraveloituksen yleiskatsaus](sepa-direct-debit-overview.md) 

[Luo suoraveloitusvaltakirja asiakkaalle](tasks/create-direct-debit-mandate-customer.md) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
