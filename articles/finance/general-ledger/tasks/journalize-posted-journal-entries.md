---
title: Kirjaa kirjatut kirjauskansioviennit
description: Tässä menettelyssä käsitellään kirjattujen kirjauskansiovientien kirjaaminen.
author: aprilolson
ms.date: 03/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8fca167563b14c825ebe29874c6488ddfb4d9a
ms.sourcegitcommit: 06acdfbccd7bd213a2397ea7b85d104f01914437
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/10/2022
ms.locfileid: "8400872"
---
# <a name="journalize-posted-journal-entries"></a>Kirjattujen kirjauskansiovientien kirjaaminen

[!include [banner](../../includes/banner.md)]

Kirjanpidon kirjausprosessi mahdollistaa kirjanpidon kirjattujen tositemerkintöjen ryhmittelyn ja raportoinnin. Ehdot määrität, käsittely luo tositteiden luettelon, joka käyttää yksilöivää numerosarjaa ja joiden viitteenä on kirjanpidon **kirjauskansion numeroarvo**.

Noudata seuraavia vaiheita kirjattujen kirjauskansiovientien kirjaamiseksi. Menettely käyttää esittelytietojen **USMF**-yritystä.

1. Siirry kohtaan **Kirjanpito** \> **Kirjanpidon asetukset** \> **Kirjanpitoparametrit**.
2. Valitse arvo **Laajennetun kirjanpidon kirjauskansio** -kentästä. Jos valitset **Kyllä**, raportin tiedot ovat erilaisia.
3. Valitse, voiko kauden sulkea, jos kirjaamisprosessia ei ole suoritettu. Jos valitset **Kyllä**, aikajaksoa ei voi sulkea, ennen kuin jakson kirjaamisprosessi on valmis.
4. Sulje sivu.
5. Siirry kohtaan **kirjanpito** \> **kausittaiset tehtävät** \> **kirjaaminen** ja valitse **Suodata**.
6. Valitse rivi, jolle haluat määrittää suodatusehdot.
7. Syötä tai valitse suodatusehdot **Ehdot**-kenttään.
8. Sulje sivu valitsemalla **OK**.
9. Aloita kirjausprosessi valitsemalla **OK**. Raportti luodaan, kun prosessi on valmis.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
