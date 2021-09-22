---
title: Klusteriin ei löydy tarpeeksi töitä profiilin määrittämisen jälkeen
description: Jos määrität klusteriprofiilin, näyttöön saattaa tulla virhesanoma, jossa todetaan, että töitä ei ole tarpeeksi. Muokkaa profiilia ja määritä Aktivoi sijainnit -kohdan arvoksi Ei.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476194"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Klusterille ei löydy tarpeeksi työtä järjestelmäohjattu klusterikeräilyä käytettäessä

## <a name="symptoms"></a>Oireet

Jos käytät *Järjestelmäohjattu klusterikeräily* -prosessia määrittäessäsi klusteriprofiilin, jossa voidaan kerätä esimerkiksi 10 paikkaa, prosessi toimii suunnitellusti, kun töitä on riittävästi 10 paikkaan keräilyyn. Jos kerättävänä on kuitenkin vain kahdeksan paikkaa, saat seuraavan virhesanoman:

> Klusteriin ei löydy riittävästi työtä.

## <a name="resolution"></a>Ratkaisu

Korjaa tämä ongelma muokkaamalla klusteriprofiilia ja määrittämällä **Aktivoi toimet** -asetukseksi *Ei*.
