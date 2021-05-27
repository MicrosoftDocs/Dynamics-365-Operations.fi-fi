---
title: Mallia ei voi käyttää vapautettuun tuotteeseen
description: Mallia ei voi käyttää vapautettuun tuotteeseen.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026466"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>Mallia ei voi käyttää vapautetun tuotteen luomiseen.

Tietopankin numero: 4612097

## <a name="symptoms"></a>Oireet

Kun luot uuden vapautetun tuotteen käyttämällä **Uusi vapautettu tuote** -valintaikkunaa, voit valita mallin. Mallin tulisi määrittää oletusasetukset monille uuden vapautetun tuotteen kentille. Joitakin kenttiä tai kaikkia kenttiä ei kuitenkaan voi määrittää mallin valitsemisen jälkeen.

## <a name="cause"></a>Syy

Monella Microsoft Dynamics 365 Supply Chain Managementin sivulla voit luoda mallin, jossa määritetään sivuilla näkyvien tietueiden alkuasetukset. Voit luoda yhden näistä malleista valitsemalla **Tietueen tiedot** toimintoruudun **Asetukset**-välilehdessä. Vapautetut tuotteet ovat kuitenkin paljon monimutkaisempia kuin useimmat muut tietueet. Vaikka voitkin luoda mallin valitsemalla **Vapautetut tuotteet** -sivulla **Tietueen tiedot** ja voit valita tämän mallin vapautetun tuotteen luomiseen, malli ei tarjoa uuden vapautetun tuotteen odotettuja kenttäarvoja. Siksi vapautettujen tuotteiden tietuetietomalleja ei voi käyttää. Sen sijaan on luotava erilliset tuotemallit.

## <a name="resolution"></a>Ratkaisu

Voit luoda tuotemallin käyttämällä toimintoruudun **Tuote**-välilehden **Malli**-valikkoa, ei **Asetukset**-välilehden **Tietueen tiedot** -painiketta.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse toimintoruudun **Tuote**-välilehden **Uusi**-ryhmästä **Malli** ja valitse sitten tarpeen mukaan joko **Luo henkilökohtainen malli** tai **Luo jaettu malli**.
