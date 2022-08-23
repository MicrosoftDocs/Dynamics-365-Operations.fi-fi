---
title: Tapahtumasähköpostien mukauttaminen toimitustilan mukaan
description: Tässä artikkelissa kuvataan, kuinka voit määrittää mukautettuja sähköpostimalleja tiettyjä ilmoitustyyppejä ja toimitustapoja varten Microsoft Dynamics 365 Commercessa.
author: bicyclingfool
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 0c0bd218c10a373d142ddcc7780c5339569f7a07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275701"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Tapahtumasähköpostien mukauttaminen toimitustilan mukaan

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka voit määrittää mukautettuja sähköpostimalleja tiettyjä ilmoitustyyppejä ja toimitustapoja varten Microsoft Dynamics 365 Commercessa.

Tapahtumakohtaisia sähköposteja voi nyt mukauttaa ilmoitustyypin (esimerkiksi **Tilauksen luonti**, **Tilaus pakattu** tai **Tilaus laskutettu**) ja toimitustavan yhdistelmän mukaan (esimerkiksi yön yli, myymälästä nouto tai nouto tien reunasta). Mukautettujen tapahtumasähköpostien avulla vähittäiskauppiaat voivat tarjota asiakkailleen tilauksen toimitustavan mukaan räätälöityjä kokemuksia. Esimerkiksi Tilaus pakattu -tapahtumaa voidaan mukauttaa niin, että se sisältää tien vierestä noudon ohjeet asiakkaille, jotka valitsevat tien vierestä noudon. Vaihtoehtoisesti se voi tarjota rahdinkuljettajan ja toimituksen tiedot asiakkaille, jotka päättävät, että tilaus lähetetään.

> [!NOTE]
> Jotta voisit käyttää mukautettuja tapahtumasähköposteja, sinun on ensin otettava käyttöön **Mukauta tapahtumasähköpostimallit toimitustavan mukaan** siirtymällä kohtaan **Työtilat \> Ominaisuuksien hallinta** Commerce-pääkonttorisovelluksessa.

Sähköposteja voi mukauttaa toimitustavan mukaan seuraaville ilmoitustyypeille:

- **Tilauksen peruutus** – Tämä sähköposti-ilmoituksen tyyppi on uusi.
- **Tilaus luotu**
- **Tilaus vahvistettu**
- **Tilaus laskutettu** – Tämä sähköposti-ilmoituksen tyyppi on uusi. Sitä voidaan käyttää **Tilaus lähetetty** -ilmoitustyypin asemesta, joka lähettää ilmoituksen mille tahansa laskutapahtumalle, jossa on lähetystoimitustapa (ei nouto tai sähköinen toimitustapa).
- **Tilaus keräilty**
- **Tilaus pakattu**
- **Tilaus valmis noudettavaksi** – Tätä ilmoitus tyyppiä voi mukauttaa toimitustavan mukaan vain, jos **Useiden noutotoimitustapojen tuki** -ominaisuus on otettu käyttöön. Tässä tapauksessa tämä ilmoitustyyppi vastaa toiminnallisesti **Tilaus pakattu** -ilmoitustyyppiä.
- **Maksu epäonnistui**
- **Luotiin korvaava tilaus**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>Tiettyjen toimitustapojen sähköpostimallien määrittäminen

Tässä menetelmässä oletetaan, että olet jo luonut uudet mukautetut sähköpostimallit ja lisännyt ne **Organisaation sähköpostimallit** -sivulle. Lisätietoja sähköpostimallien luomisesta ja lataamisesta palvelimeen on kohdassa [Sähköpostimallien luominen tapahtumille](email-templates-transactions.md).

Voit määrittää tiettyjen toimitustapojen sähköpostimallit Commerce-pääkonttorisovelluksessa noudattamalla seuraavia ohjeita.

1. Siirry **Commerce-sähköpostiprofiili** -kohtaan.
1. Valitse aiemmin luotu ilmoitustyyppi **Vähittäismyyntitapahtuman ilmoitusasetukset** -kohdassa.
1. Kun ilmoitustyyppi on edelleen valittuna, valitse **Määritä toimitustavat**.
1. Valitse **Toimitustavat**-valintaruudussa **Uusi**.
1. Valitse uudella rivillä **Toimitustapa**-kentässä toimitustapa.
1. Valitse **Sähköpostin tunnus** -kentästä sähköpostimalli, jonka haluat yhdistää toimitustapaan.
1. Valitse **Käytössä**-valintaruutu.
1. Voit lisätä uusia toimitustapoja toistamalla vaiheet 4–7.
1. Kun olet valmis, valitse **OK**.

> [!NOTE]
> - Jos myyntitilauksen riveillä on useita toimitustapoja, käytetään oletusmallia. Oletusmalli on malli, joka on yhdistetty ilmoitustyyppiin **Commerce-sähköposti-ilmoituksen profiili** -sivulla.
> - Jos myyntitilauksessa on toimitustapa, jota ei ole määritetty mukautetulle sähköpostimallille, käytetään oletussähköpostimallia.

## <a name="additional-resources"></a>Lisäresurssit

[Puhelinkeskustilausten luominen](tasks/create-call-center-orders.md)

[Toimitustavan muuttaminen myyntipisteessä](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
