---
title: Sarjanumeron avulla seurattujen tuotteiden palauttaminen myyntipisteessä
description: Tässä artikkelissa kuvataan ominaisuuksia, joita voi käyttää sarjallistettujen nimikkeiden tarkistamiseen osana Microsoft Dynamics 365 Commerce -myyntipistesovelluksen palautusprosessia.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9fa7e47b6d650370afe4b98d7eca01253bd1bc36
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268471"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Sarjanumeron avulla ohjattujen tuotteiden palautus myyntipisteessä

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan ominaisuuksia, joita voi käyttää sarjallistettujen nimikkeiden tarkistamiseen osana Microsoft Dynamics 365 Commerce -myyntipistesovelluksen palautusprosessia.

> [!NOTE]
> Commerce-versiossa 10.0.20 ja sitä myöhemmissä versioissa on uusi toiminto nimeltä **Myyntipisteen yhdistetty palautuksen käsittelykokemus**. Sarjanumeron oikeellisuustarkistuksen käyttäminen palautustilauksen käsittelyn aikana myyntipisteessä edellyttää, että tämä toiminto on otettava käyttöön. Lisätietoja muista ominaisuuksista, joita tämä ominaisuus tarjoaa, kun se on käytössä: [Palautusten luominen myyntipisteessä](POS-returns.md).
>
> Kun toiminto on otettu käyttöön, sitä ei voi poistaa käytöstä.

## <a name="options-for-validating-serialized-returns"></a>Sarjoitettujen palautusten validointiasetukset

Kun **Myyntipisteen yhdistetty palautuksen käsittelykokemus** on käytössä, organisaatiot voivat suorittaa sarjanumero-ohjattujen nimikkeiden palautusten oikeellisuustarkistuksen myyntipisteen kautta. Tämä ominaisuus voi varoittaa käyttäjiä, jos palautettava sarjanumero eroaa myydystä alkuperäisestä sarjanumerosta. Commerce-versiossa 10.0.20 ja sitä myöhemmissä versioissa käyttäjien vastaanottama sanoma on vain varoitussanoma. Käyttäjät voivat jatkaa palautusten käsittelemistä käyttäen sarjanumeroa, joka eroaa alun perin myydystä sarjanumerosta.

Kun haluat määrittää sarjanumeron tarkistuksen organisaatiolle, kun **Myyntipisteen yhdistetty palautuksen käsittelykokemus** on otettu käyttöön, siirry Commerce headquartersissa kohtaan **Vähittäismyynti ja kauppa \> Headquartersin asetukset \> Parametrit \> Commerce-parametrit**. Määritä **Varasto**-välilehden **Myymälän varastotoiminnot** -pikavälilehdessä **Ota käyttöön sarjanumeroiden tarkistus myyntipistepalautuksissa** -vaihtoehdon arvoksi **Kyllä**.

## <a name="process-returns-for-serialized-items-in-pos"></a>Sarjoitettujen nimikkeiden palautusten käsitteleminen myyntipisteessä

Jos **Ota käyttöön sarjanumeroiden tarkistus myyntipistepalautuksissa** -asetukseksi on määritetty **Kyllä**, kun sarjanumerolla ohjattava nimike palautetaan myyntipisteen kautta, käyttäjä voi syöttää palautusrivin sarjanumeron **Palautuskelpoiset tuotteet** -sivun tietoruutuun. Jos syötetty sarjanumero ei vastaa myyntitapahtumassa myytyä alkuperäistä sarjanumeroa, näyttöön tulee varoitussanoma. Sovellus ei kuitenkaan estä käyttäjää kirjaamasta palautusta edelleen.

> [!NOTE]
> Tällä hetkellä myyntipiste tukee sarjanumeroiden oikeellisuustarkistusta vain palautusriveillä, joissa alkuperäinen tilattu määrä ei ole enempää kuin yksi. Jos alkuperäinen myyntitilausrivi on luotu muussa kuin myyntipistekanavassa ja jos sarjoitetulle nimikkeelle tilattu määrä on enemmän kuin yksi, nimikettä ei voi palauttaa oikein myyntipisteen kautta.

## <a name="additional-resources"></a>Lisäresurssit

[Palautusten luominen myyntipisteessä](POS-returns.md)
