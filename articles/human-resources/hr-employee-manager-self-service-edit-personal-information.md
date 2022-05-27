---
title: Muokkaa henkilökohtaisia tietoja
description: Tässä artikkelissa kuvataan, miten henkilötietoja muokataan työntekijän ja esimiehen itsepalvelussa.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d7e78873d0995334ac80ac22e8058b7fe0bc31ac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686119"
---
# <a name="edit-personal-information"></a>Henkilökohtaisten tietojen muokkaaminen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit muokata henkilötietojasi Dynamics 365 Human Resourcesissa **Työntekijän itsepalvelu** -työtilassa.

Voit muokata myös seuraavia henkilökohtaisia tietoja:

- Osoitteet
- Yhteyshenkilön tiedot
- Henkilökohtaiset yhteyshenkilöt
- Tunnusnumerot
- Maksutapa
- Henkilöstöhallinnossa käytettävä kuva

>[!NOTE]
>Et välttämättä voi muokata kaikkia henkilökohtaisia tietoja, kuten yrityksen yhteystietoja. Lisätietoja on kohdassa [Henkilökohtaisten tietojen muokkaamisen rajoittaminen](hr-employee-self-service-restrict-editing.md).

**Yleisen osoitekirjan parametrit** -sivulla määritetyt parametrit määrittävät roolit, jotka voivat tarkastella henkilökohtaisia tietojasi.

1. Valitse henkilöstöhallinnossa **Työntekijän itsepalvelu**.

2. Valitse **Muokkaa henkilökohtaisia tietoja**.

3. Jos haluat muuttaa osoitetta, valitse **Osoitteet** -välilehti. Tekemäsi muutokset näkyvät **Henkilöstöhallinnan** työtilassa ja varoittavat henkilöstöhallintoa.

    - Valitse **Lisää** lisätäksesi uuden osoitteen.
    - Jos haluat muokata aiemmin luotua osoitetta, valitse osoite ja valitse sitten **Muokkaa**.
    - Jos haluat tarkastella karttaa, valitse **Kartta**.
    - Voit lisätä tai poistaa yhteystiedon valitsemalla **Lisää asetuksia** ja valitsemalla sitten **Lisäasetukset**. Valitse **Yhteystiedot**-kohdasta **Lisää** tai **Poista** ja muokkaa kenttiä tarpeen mukaan.
    - Jos haluat määrittää aikavyöhykkeen ja sijainnin, valitse **Lisää asetuksia** ja valitse sitten **Lisäasetukset**. Muokkaa **Yleiset**-kohdan kenttiä tarpeen mukaan.

4. Voit muuttaa yhteystietoja valitsemalla **Yhteystiedot**-välilehden. Voit määrittää erityyppisiä yhteystietoja, kuten puhelin-, sähköposti- ja sosiaalisen median linkkejä. Voit määrittää yhteystiedot ensisijaiseksi, mutta voit määrittää vain yhden kunkin tyypin ensisijaiseksi vaihtoehdoksi.

    - Valitse **Lisää** lisätäksesi uuden yhteystiedon. Muokkaa kenttiä tarvittavalla tavalla.
    - Jos haluat muokata aiemmin luotua yhteystietoa, valitse nimike ja valitse sitten **Muokkaa**. Muokkaa kenttiä tarvittavalla tavalla.
    - Voit määrittää yhteystiedon yksityiseksi valitsemalla kohteen, valitsemalla **Lisäasetukset** ja määrittämällä sitten **Yksityisen** vaihtoehdon arvoksi **Kyllä**. Valitse **OK**.
      >[!NOTE]
      >**Lisäasetukset**-painike ei ole käytettävissä, jos järjestelmänvalvojasi on ottanut **(Esikatselu) Estä työntekijöitä lisäämästä tai muokkaamasta osoite- ja yhteystietoja tiettyihin tarkoituksiin** -ominaisuuden käyttöön ympäristössäsi. Lisätietoja on kohdassa [Henkilökohtaisten tietojen muokkaamisen rajoittaminen](hr-employee-self-service-restrict-editing.md).
  
5. Voit muuttaa henkilökohtaisia yhteystietoja valitsemalla **Omat yhteystiedot** -välilehden. Voit määrittää hätäyhteyshenkilöitä, edunsaajia ja huollettavia. Yhteystieto voi olla henkilö tai organisaatio. **Etujen hallinta** -toiminto käyttää henkilökohtaisia yhteystietoja. Katso lisätietoja kohdasta [Henkilökohtaisten yhteyshenkilöiden oikeutusasetusten määrittäminen](hr-benefits-setup-contact-eligibility-options.md).

6. Jos haluat muuttaa tunnusnumeroita, kuten henkilötunnusta, valitse **Tunnusnumerot**-välilehti. Muutokset voivat käydä läpi hyväksyntäprosessin, jos organisaatio on määrittänyt hyväksynnän työnkulun.

    - Voit lisätä tunnusnumeron valitsemalla **Uusi**. Täytä tarvittavat kentät ja valitse **Tallenna**.
    - Jos haluat muokata numeroa, valitse **Muokkaa**. Muokkaa tarvittavat kentät ja valitse **Tallenna**.

7. Jos haluat muuttaa maksutapoja, valitse **Omat maksutiedot** -välilehti. Tämä välilehti on käytettävissä vain, jos maksutavat ovat käytössä **Henkilöstöhallinnon parametrit** -sivulla. HR voi ottaa käyttöön **pankkiluonnoksen**, **käteisen**, **sekin**, **sähköisen maksamisen** tai **muun**. HR voi myös poistaa käytöstä sähköisen maksun vahvistuksen (käytetään Yhdysvaltain palkanlaskennassa) sekä pankkitilin ja reititysnumeron oikeellisuustarkistuksen.

8. Jos haluat vaihtaa henkilöstöhallinnossa näkyvän profiilikuvan, valitse **Kuva**-välilehti. Organisaation asetuksista riippuen kuvat saatetaan reitittää hyväksyttäväksi.

    - Lataa kuva valitsemalla **Lataa uusi kuva**.
    - Jos haluat poistaa kuvan, valitse kuva ja valitse sitten **Poista**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
