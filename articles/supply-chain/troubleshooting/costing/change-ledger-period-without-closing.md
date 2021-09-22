---
title: Varoitukset tai virheet, kun kirjanpitokauden tila muutetaan varastoa sulkematta
description: Varoitukset tai virheet, kun kirjanpitokauden tila muutetaan varastoa sulkematta
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476214"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Varoitukset tai virheet, kun kirjanpitokauden tila muutetaan varastoa sulkematta

Microsoft otti seuraavat vahvistukset käyttöön estämään ongelmat, joita kustannuslaskennan virheellinen kauden lopetusprosessi aiheuttaa. Jos jokin seuraavista virhesanomista avautuu, lisätietoja näiden ongelmien ratkaisemisesta on tietoartikkelissa [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3).

- Olet suorittamassa uudelleenlaskennan päivämäärällä %1 (10-02-2019). Viimeksi rekisteröity uudelleenlaskenta suorittiin edellisellä kaudella päivämäärällä %2 (20-01-2019). Varaston sulkemista ei suoriteta päivämäärällä %3 (31-01-2019), jolla kohdistuskauden loppu on rekisteröity. Muista suorittaa varaston sulkeminen alkaen päivämäärästä %3 (31-01-2019), jolloin kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu.

- Olet muuttamassa kirjanpitokauden tila %1 tilaksi %2. Varaston sulkemista ei suoriteta päivämäärällä %3, jolla kohdistuskauden loppu on rekisteröity. Suorita varaston sulkeminen alkaen %3 kohdistuskauden lopusta ennen tilan muuttamista. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu. Raportoidaan yrityksestä %4. Toistaiseksi tämä on vain tiedoksi, mutta vastaisuudessa sinun on suoritettava tällainen toiminto.

- Tilirakennetta %1on muutettu. Vähintään yhtä päätiliä %2 ei enää ole. %3 tarvitsee näitä päätilejä päivämäärällä %4. Lisää nämä päätilit tilirakenteeseen %1 ennen työn %3 jatkamista. Toistaiseksi tämä on vain tiedoksi, mutta vastaisuudessa sinun on suoritettava tällainen toiminto.

- Olet sulkemassa varaston päivämäärällä %1(31-01-2019). Jälkikustannuslaskentaa ei suoriteta päivämäärällä %2 (31-01-2019), jolla kohdistuskauden loppu on rekisteröity. Muista suorittaa jälkikustannuslaskentaa päivämäärällä %3 (31-01-2019), jolla kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu.

- Olet suorittamassa jälkikustannuslaskennan päivämäärällä %1 (28-02-2019). Viimeksi rekisteröity jälkikustannuslaskenta suorittiin edellisellä kaudella päivämäärällä %2 (31-01-2019). Varaston sulkemista ei suoriteta päivämäärällä %3 (31-01-2019), jolla kohdistuskauden loppu on rekisteröity.

Muista suorittaa varaston sulkeminen alkaen %3 (31-01-2019), jolloin kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes varaston sulkeminen on suoritettu.