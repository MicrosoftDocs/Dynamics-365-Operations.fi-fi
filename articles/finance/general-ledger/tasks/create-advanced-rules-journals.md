---
title: Luo kirjauskansioiden lisäsäännöt
description: Tässä menettelyssä käsitellään kirjauskansioiden lisäsääntöjen luontia.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3eb34ac419aeab3663a8931d022abf7bcbfddd37
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186230"
---
# <a name="create-advanced-rules-for-journals"></a>Luo kirjauskansioiden lisäsäännöt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään kirjauskansioiden lisäsääntöjen luontia. Niitä ovat esimerkiksi kirjauskansion hallinnan ja käyttäjän kirjausrajoitusten määrittäminen. Menettely käyttää USMF-yrityksen demotietoja.


## <a name="set-up-journal-control"></a>Määritä kirjauskansion hallinta
1. Siirry kohtaan **Siirtymisruutu** > **Moduulit > kirjanpito > kirjauskansion asetukset > Kirjauskansioiden nimet**.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta **Toimintoruudussa** **Kirjauskansion hallinta**.
4. Valitse **Mitä tilityyppejä voidaan kirjata** -pikavälilehdessä **Lisää**.
5. Avaa haku napsauttamalla **Yrityksen tilit** -kentässä avattavan valikon painiketta.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Valitse **Mitkä segmenttiarvot ovat kelvollisia tälle kirjauskansiolle** -pikavälilehdessä **Lisää**.
9. Avaa haku napsauttamalla **Tilirakenne**-kentässä avattavan valikon painiketta.
10. Etsi haluamasi tietue luettelosta ja valitse se.
11. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
12. Avaa haku napsauttamalla **Segmentti**-kentässä avattavan valikon painiketta.
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
14. Avaa haku napsauttamalla **Arvosta**-kentässä avattavan valikon painiketta.
15. Etsi haluamasi tietue luettelosta ja valitse se.
16. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
17. Avaa haku valitsemalla **Arvoon**-kentässä avattavan valikon painike.
18. Etsi haluamasi tietue luettelosta ja valitse se.
19. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="set-up-posting-restrictions"></a>Kirjausrajoitusten määrittäminen
1. Sulje sivu.
2. Valitse **Kirjausrajoitukset**.
3. Valitse **Miten haluat määrittää kirjaamisrajoitukset** -asetukseksi Käyttäjäryhmäkohtainen.
4. Valitse puussa ryhmä, jolle annat luvan kirjata tähän kirjauskansioon.
5. Valitse **OK**.

