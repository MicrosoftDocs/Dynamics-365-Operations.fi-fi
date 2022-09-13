---
title: Varastotyön peruutus poikkeusten käsittelyä varten
description: Tässä artikkelissa kuvaillaan työn peruutustoiminto, jonka avulla varastojen esimiehet voivat käsitellä estynyttä työtä.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b1e2036e4e7a8a47d6df029f285df7aca0fa74e6
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403680"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Varastotyön peruutus poikkeusten käsittelyä varten

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Managementin työn peruutustoiminnon avulla järjestelmänvalvoja voi peruuttaa tietyn käynnissä olevan varastotyön, jonka järjestelmä on estänyt tai jota ei voida suorittaa loppuun erityisolosuhteiden vuoksi. Tämä toiminto on houkutteleva ja turvallinen vaihtoehto korjaaville SQL-komentosarjoille, jotka korjaavat epäyhtenäisiä tietoja. Vaikka näitä komentosarjoja pyydetään yleensä IT-ammattilaisilta, työn peruutustoimintoa voivat käyttää yrityksen käyttäjät, joilla on järjestelmänvalvojan oikeudet.

Voit käyttää työn peruutustoimintoa kohdassa **Varastonhallinta** \> **Kausittaiset tehtävät** \> **Puhdista \> Peruuta työ**. Määritä peruutettavan työn työtunnus **Peruuta työ** -valintaikkunassa ja valitse **OK**.

## <a name="warehouse-work-that-can-be-canceled"></a>Varastotyöt, jotka voidaan peruuttaa

Varaston keräilytoimien yhteydessä työntekijä voi kohdata tilanteita, jossa hän on rekisteröinyt määriä kerätyksi varastointipaikasta käyttäjäpaikkaansa, mutta ei voi rekisteröidä asetustoimea. Epäyhtenäiset varastotiedot ovat usein, mutta eivät aina, syynä työn estymiseen.

Toisin kuin tavanomainen työn peruutustoiminto, jota voidaan käyttää työotsikon **Peruuta**-painikkeella, työn peruutustoiminto ei edellytä, että viimeinen valmis työrivi on **Astus**-tyypin työrivi. Toisin sanoen peruutuslogiikka voidaan suorittaa työn peruutustoiminnon osalta, vaikka työrivin nimikemäärä on käyttäjäsijainnissa.

> [!NOTE]
> Toiminnallisista syistä peruutettavassa työssä varaston käyttäjien on edelleen käytettävä työsivun tavallista peruutustoimintoa.

Työn peruutustoimintoa voidaan käyttää vain **Myynti**-, **Siirtovarasto-otto**-, **Raaka-aineiden keräily**- ja **Täydennys**-tyyppisen työn peruuttamiseen. Peruutuslogiikka ei suoriteta jäädytettyjen raaka-aineiden keräilytöiden osalta eikä sellaisten töiden osalta, jotka voidaan peruuttaa tavallisella peruutustoiminnolla (katso edellinen huomautus).

Saadakseen työn jatkumaan järjestelmä peruuttaa jäljellä olevat työrivit ja korjaa käyttäjän määrittämään työtunnukseen liittyvät varastotiedot. Tämän jälkeen tavalliset varaston käsittelytoimet, jotka kohdistuvat aiemmin estyneeseen nimikemäärään, voivat jatkua.

Asettaakseen aiemmin estyneen nimikkeen tiettyyn sijaintiin työn peruuttamisen jälkeen käyttäjän on käytettävä varaston siirtotapahtumaa tai määrän oikaisua mobiililaitteella.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]