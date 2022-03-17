---
title: Luo Azure-tallennustili Azure-portaalissa
description: Tässä ohjeaiheessa kerrotaan, miten luodaan Azure-tallennustili sähköiselle laskutukselle.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3d9647e234b3603ef6305ec6031a793b744bbe98
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371681"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Luo Azure-tallennustili Azure-portaalissa

[!include [banner](../includes/banner.md)]

Kaikki sähköisen laskutuspalvelun luomat tai palveluun käsittelyn aikana menevät sähköiset tiedostot tallennetaan Microsoft Azure -tallennustilisi säilöihin. Jotta voidaan varmistaa, että sähköinen laskutus voi käyttää näitä säilöjä, sinun on annettava tallennustilin jaetun käyttöoikeuden allekirjoituksen (SAS) tunnus sähköisen laskutuksen palvelulle. Voit myös varmistaa, että tunnus on tallennettu suojatusti, kun SAS-tunnusta ei anneta suoraan. Tallenna sen sijaan se Azure Key Vaultiin ja määritä Azure Key Vaultin salainen koodi.

1. Avaa tallennustili, jota aiot käyttää sähköisen laskutuksen palvelun kanssa.
2. Siirry kohtaan **Asetukset** \> **Määritys** ja varmista, että **Salli Blob-objektin julkinen käyttö** -parametriksi on määritetty **Käytössä**.
3. Siirry kohtaan **Tietojen tallennus** \> **Kontit** ja luo uusi kontti.
4. Anna säilölle nimi ja määritä **Julkinen käyttöoikeustaso** -kentän arvoksi **Yksityinen (ei anonyymia käyttöä)**.
5. Avaa uusi säilö ja siirry kohtaan **Asetukset** \> **Käyttöoikeuskäytäntö**.
6. Valitse **Lisää käytäntö** lisätäksesi tallennetun käyttöoikeuskäytännön.
7. Määritä **Tunnus**-kenttä tarpeen mukaan.
8. Valitse **Oikeudet**-kentässä kaikki oikeudet.

    ![Käyttöoikeudet-kentässä Lisää käytäntö -valintaikkunassa valittuna kaikki käyttöoikeudet.](media/e-invoicing-azure-1.png)

9. Määritä alkamis- ja päättymispäivät. Päättymispäivän on oltava tulevaisuudessa.
10. Tallenna käytäntö valitsemalla **OK** ja tallenna muutoksesi säilöön.
11. Siirry kohtaan **Asetukset** \> **Jaetut käyttöoikeustietueet** ja määritä kenttien arvot.
12. Määritä alkamis- ja päättymispäivät. Päättymispäivän on oltava tulevaisuudessa.
13. Valitse **Oikeudet**-kentässä seuraavat oikeudet:

    - Lue
    - Lisää
    - Luo
    - Kirjoita
    - Poista
    - Luettelo

14. Valitse **Luo SAS-tunnus ja URL**.
15. Kopioi arvo ja tallenna se **Blob-SAS-URL**-kenttään. Tätä arvoa käytetään myöhemmin tässä menettelyssä, ja sitä kutsutaan *jaetun käyttöoikeuden allekirjoituksen URI-tunnukseksi*.
16. Avaa avainsäilö, jota aiot käyttää sähköisen laskutuksen kanssa.
17. Siirry kohtaan **Asetukset** \> **Salasanat** ja luo sitten salasana valitsemalla **Luo/tuo**.
18. Valitse **Luo salasana** -sivun **Lataa asetuksia** -kentässä **Manuaalinen**.
19. Anna salasanan nimi. Tätä nimeä käytetään palvelun määrittämiseen RCS:ssä (Regulatory Configuration Service) ja sitä kutsutaan *avainsäilön salasananimeksi*. Lisätietoja RCS:n määrittämisestä: [Regulatory Configuration Servicesin (RCS) määritys](e-invoicing-set-up-rcs.md).
20. Liitä **Arvo**-kenttään aiemmin kopioitu jaetun käyttöoikeuden allekirjoituksen URI-tunnus.
21. Valitse **Luo**.
