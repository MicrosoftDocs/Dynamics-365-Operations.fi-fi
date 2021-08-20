---
title: Varastotyön peruutus poikkeusten käsittelyä varten
description: Tässä aiheessa kuvaillaan Peruuta työ -toiminto, jonka avulla varastojen esimiehet voivat käsitellä estynyttä työtä.
author: omulvad
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3cab74b1961213567d0caa49035048cb84cffddeb13b63bfc699f4f130f08c77
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775480"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Varastotyön peruutus poikkeusten käsittelyä varten

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Managementin Peruuta työ -toiminnon avulla järjestelmänvalvoja voi peruuttaa tietyn käynnissä olevan varastotyön, jonka järjestelmä on estänyt tai jota ei voida suorittaa loppuun erityisolosuhteiden vuoksi. Tämä toiminto on houkutteleva ja turvallinen vaihtoehto korjaaville SQL-komentosarjoille, jotka korjaavat epäyhtenäisiä tietoja. Vaikka näitä komentosarjoja pyydetään yleensä IT-ammattilaisilta, Peruuta työ -toimintoa voivat käyttää yrityksen käyttäjät, joilla on järjestelmänvalvojan oikeudet.

Voit käyttää Peruuta työ -toimintoa kohdassa **Varastonhallinta** \> **Kausittaiset tehtävät** \> **Puhdista \> Peruuta työ**. Määritä peruutettavan työn työtunnus **Peruuta työ** -valintaikkunassa ja valitse **OK**.

## <a name="warehouse-work-that-can-be-canceled"></a>Varastotyöt, jotka voidaan peruuttaa

Varaston keräilytoimien yhteydessä työntekijä voi kohdata tilanteita, jossa hän on rekisteröinyt määriä kerätyksi varastointipaikasta käyttäjäpaikkaansa, mutta ei voi rekisteröidä asetustoimea. Epäyhtenäiset varastotiedot ovat usein, mutta eivät aina, syynä työn estymiseen.

Toisin kuin tavanomainen Peruuta-toiminto, jota voidaan käyttää työotsikon **Peruuta**-painikkeella, Peruuta työ -toiminto ei edellytä, että viimeinen valmis työrivi on **Astus**-tyypin työrivi. Toisin sanoen peruutuslogiikka voidaan suorittaa Peruuta työ -toiminnon osalta, vaikka työrivin nimikemäärä on käyttäjäsijainnissa.

> [!NOTE]
> Toiminnallisista syistä peruutettavassa työssä varaston käyttäjien on edelleen käytettävä työsivun tavallista Peruuta-toimintoa.

Peruuta työ -toimintoa voidaan käyttää vain tyyppien **Myynti**, **Siirtovarasto-otto**, **Raaka-aineiden keräily** tai **Täydennys** työn peruuttamiseen. Peruutuslogiikka ei suoriteta jäädytettyjen raaka-aineiden keräilytöiden osalta eikä sellaisten töiden osalta, jotka voidaan peruuttaa tavallisella Peruuta-toiminnolla (katso edellinen huomautus).

Saadakseen työn jatkumaan järjestelmä peruuttaa jäljellä olevat työrivit ja korjaa käyttäjän määrittämään työtunnukseen liittyvät varastotiedot. Tämän jälkeen tavalliset varaston käsittelytoimet, jotka kohdistuvat aiemmin estyneeseen nimikemäärään, voivat jatkua.

Asettaakseen aiemmin estyneen nimikkeen tiettyyn sijaintiin työn peruuttamisen jälkeen käyttäjän on käytettävä varaston siirtotapahtumaa tai määrän oikaisua mobiililaitteella.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]