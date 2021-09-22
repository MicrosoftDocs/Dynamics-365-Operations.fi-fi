---
title: Yhdistelmärekisterikilven vastaanottoa ei toimi kaikkien käsittelykoodien yhteydessä
description: Kun jakelukoodin Toiminto-kentän määrityksenä on Hyvitys tai Hävikki, voit käyttää Yhdistelmärekisterikilven vastaanotto -valikkovaihtoehtoa palautettujen nimikkeiden käsittelemiseen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476253"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>Yhdistelmärekisterikilven vastaanottoa ei voi käyttää muussa kuin hyvityksen jakelukoodissa

## <a name="symptoms"></a>Oireet

Kun jakelukoodin **Toiminto**-kentän määrityksenä on *Hyvitys* tai *Hävikki*, voit käyttää [Yhdistelmärekisterikilven vastaanotto](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving) -valikkovaihtoehtoa palautettujen nimikkeiden käsittelemiseen.

## <a name="resolution"></a>Ratkaisu

Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus. Tällä hetkellä yhdistelmärekisterikilven vastaanotossa tuetaan vain [jakelukoodeja](/dynamics365/supply-chain/service-management/set-up-disposition-codes), joissa **Toiminto**-kentän asetuksena on *Hyvitys* tai *Hävikki*.
