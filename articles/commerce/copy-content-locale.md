---
title: Sisällön kopioiminen toiselle kielialueelle
description: Tässä artikkelissa käsitellään aiemmin luodun sisällön kopioimista sivustossa toiselle kielialueelle Microsoft Dynamics 365 Commercen sivustonmuodostimessa.
author: josaw1
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6afa871048bde22133ae083b8d56b6e99e49c401
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269258"
---
# <a name="copy-content-to-another-locale"></a>Sisällön kopioiminen toiselle kielialueelle

[!include[banner](../includes/banner.md)]

Tässä artikkelissa käsitellään aiemmin luodun sisällön kopioimista sivustossa toiselle kielialueelle Microsoft Dynamics 365 Commercen sivustonmuodostimessa.

Kun Commercen sivustonmuodostimessa luodaan sisältöä, siihen voidaan aina liittää kielialueen tunnus, kuten en-us. Yksittäisiä sivuja tai resursseja voidaan kopioida samassa sähköisessä kaupankäyntisivustossa olevalle kielialueelle vaihtamalla kielialuetta, kun sisältökohdetta muokataan ja luomalla sitten kohteesta uuden variantin. Joissakin tapauksissa, kuten käynnistettäessä täysin uutta kielialuetta kaupassa, kaikki aiemmin luodun kielialueen sisältökohteet kannattaa monistaa uudelle kielialueelle. Jos uudella kielialueella on sama pääkieli kuin jollakin aiemmin luoduista kielialueista, aiemmin luotua kielialuetta voidaan käyttää lähdekielialueena kielialueen kopiointitoiminnossa. (Esimerkiksi sekä en-us- että en-au-kielialueella käytetään englannin kieltä.) Tämä helpottaa sisällön lokalisointia uudelle kielialueelle.

Seuraavaksi selvitetään, miten uusi kielialue lisätään aiemmin luotuun kanavaan, miten kaikki sisältökohteet kopioidaan aiemmin luodulta kielialueelta uudelle kielialueelle ja miten kielialueen kopiointitoiminnon tilaa seurataan.

## <a name="add-a-new-locale"></a>Uuden kielialueen lisääminen

Uusi kielialue lisätään Commercen sivustonmuodostimessa seuraavasti.

1. Siirry sivustoon sivustonmuodostimessa.
1. Valitse vasemmassa siirtymisruudussa **Sivuston asetukset** ja valitse sitten **Kanavat**.
1. Valitse **Kanava**-kohdassa kanava, johon uusi kielialue lisätään.
1. Valitse oikealle avautuvassa valintaruudussa **Lisää aluekohtaiset asetukset**.
1. Valitse **Lisää aluekohtaiset asetukset** -valintaikkunan **Tuettavat aluekohtaiset asetukset** -kentässä kielialue.
1. Vahvista, että **Toimialue**-arvo on oikein.
1. Anna **Polku**-kohdassa yksilöivä URL-polku (kuten **en-us** tai **english-us**).
1. Valitse **OK**.
1. Sulje kanavan valintaikkuna.
1. Vahvista **Kanava**-kohdassa, että uusi kielialue näkyy oikean kanavan vieressä.
1. Valitse **Tallenna ja julkaise**.

> [!NOTE]
> Uutta kielialuetta ei voi määrittää sivustonmuodostimessa, ennen kuin se on lisätty liitettyyn verkkokauppakanavaan Commerce headquartersissa.

## <a name="copy-all-content-items-to-a-new-locale"></a>Kaikkien sisältökohteisen kopioiminen uudelle kielialueelle

Kaikki sisältökohteet kopioidaan uudelle kielialueella Commercen sivustonmuodostimessa seuraavasti.

1. Siirry sivustoon sivustonmuodostimessa.
1. Valitse vasemmassa siirtymisruudussa **Sivuston asetukset** ja valitse sitten **Kanavat**.
1. Valitse komentopalkissa **Luo kielialueen kopio kohteesta**.
1. Vahvista oikealle avautuvassa **Luo kielialueen kopio** -valintaikkunan **Lähdesivusto**-kohdassa, että oikea sivusto on valittu.
1. Valitse **Lähdekanava**-kentässä lähdekanava.
1. Valitse **Kohdekanava**-kentässä sama lähdekanava.
1. Valitse **Lähteen aluekohtaiset asetukset** -kentässä lähdekielialue.
1. Valitse **Kohdekielialue**-kentässä uusi kielialue.
1. Valitse **Kopioi kielialue**. Ilmoitus vahvistaa, että kielialueen kopiointitoiminto on aloitettu.

> [!NOTE]
> Sisältöä voi kopioida myös eri kanavien välillä.

## <a name="monitor-the-status-of-the-locale-copy"></a>Kielialueen kopioinnin tilan seuraaminen

Kielialueen kopiointitoiminnon tilaa voi seurata seuraavasti.

1. Siirry sivustoon sivustonmuodostimessa.
1. Valitse vasemmassa siirtymisruudussa **Sivuston asetukset** ja valitse sitten **Työt**.
1. Valitse **Nykyiset työt** -kohdassa seurattava työ. Työn tiedot näkyvät oikealle avautuvassa valintaikkunassa.
