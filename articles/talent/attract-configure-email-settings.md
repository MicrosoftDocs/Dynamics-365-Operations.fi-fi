---
title: Sähköpostiasetusten määrittäminen Attractissa
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Attractista lähetettävien sähköpostien asetusten määrittämistä.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: e641e3f0d1873d91be1a1dc9bc22eb734a2b21d5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461013"
---
# <a name="configure-email-settings-in-attract"></a>Sähköpostiasetusten määrittäminen Attractissa

[!include [banner](includes/banner.md)]

Brändisi kasvattaa luottamusta ja auttaa luomaan suhteen ehdokkaisiin, ennen kuin he hakeva työpaikkaa. Positiivinen mielikuva brändistä houkuttelee parhaat työhakijat ja parantaa nykyisten työntekijöiden uskollisuutta. Microsoft Dynamics 365 Talent: Attractin avulla voit määrittää sähköpostit yrityksen brändin mukaisiksi. Tällä tavoin työpaikkaa hakevien kokemus pysyy yhtenäisenä koko hakuprosessin ajan.

Attractin avulla voi tehdä seuraavat toimet:

- Määritä sähköpostiosoitteet niin, että yrityksen Microsoft Exchange -sähköpostipalvelutili on käytössä. Tällä tavoin hakijat tietävät, että heidän sähköpostinsa ovat yrityksen lähettämiä. Voit määrittää asetukset esimerkiksi siten, että hakijat saavat sähköpostia osoitteesta `recruiting@contoso.com` eikä `contoso@microsoft.com`.
- Yhtenäisen brändin luominen kaikelle sähköpostiviestinnälle määrittämällä yleinen ylä- ja alatunniste kaikkiin sähköpostimalleihin. 

> [!NOTE]
> Attractin määrittäminen käyttämään sähköpostin lähettämiseen yrityksen sähköpostitiliä edellyttää kattavan työhönottolaajennuksen käyttöä.

## <a name="connect-an-email-service-account"></a>Sähköpostipalvelun tilin liittäminen

Liittämällä yrityksen sähköpostipalvelun tilin voi luoda työn hakijoille brändin mukaisen sähköpostikokemuksen. Jos et liitä yritystiliäsi, Attract käyttää oletusarvoista Microsoftin sähköpostipalvelun tiliä.

1. Valitse ensin **Asetukset** (rataskuvake oikeassa yläkulmassa) ja sitten **Hallintakeskus**.
2. Valitse **sähköpostipalvelun tilien** **Sähköpostiasetukset**-välilehdessä **Liitä yritystili**.

    ![Yrityksen sähköpostipalvelun tilin liittäminen Attractissa](./media/attract-admin-email-service-accounts.png)

    Lisätietoja jaetun sähköpostitilin luomisesta on kohdassa [Exchange Onlinen jaetut postilaatikot](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).

3. Kirjaudu Microsoftin kirjautumisikkunassa sisään yrityksen tunnistetiedoilla.
4. Jos et ole vielä määrittänyt sähköpostipalvelun tiliä tai jos haluat lisätä uuden tilin, valitse **Lisää uusi palvelun tili** ja anna sitten sähköpostin tiedot. Jos olet jo määrittänyt sähköpostipalvelun tilin, jota haluat käyttää, valitse se.

Kun sähköpostipalvelun tili on määritetty, se näkyy **Sähköpostipalvelun tilit** -luettelossa.

## <a name="disconnect-an-email-service-account"></a>Sähköpostipalvelun tilin yhteyden katkaiseminen

Jos haluat lopettaa yrityksen toimialueen käyttämisen Attract-sähköpostiviestinnässä, voit katkaista sähköpostipalvelun tilin yhteyden.

1. Valitse ensin **Asetukset** (rataskuvake oikeassa yläkulmassa) ja sitten **Hallintakeskus**.
2. Valitse **sähköpostipalvelun tilien** **Sähköpostiasetukset**-välilehdessä **Lisää**-painike (kolme pistettä) sen sähköpostipalvelun tilin vieressä, jonka yhteyden haluat katkaista.
3. Valitse **Katkaise sähköpostitilin yhteys**.

    ![Yrityksen sähköpostipalvelun tilin yhteyden katkaiseminen](./media/attract-admin-disconnect-email-account.png)

4. Kun sinua pyydetään vahvistamaan toiminto, valitse **Katkaise yhteys**.

    ![Yrityksen sähköpostipalvelun tilin yhteyden katkaisemisen vahvistaminen](./media/attract-admin-email-confirm-disconnect.png)

Jos et liitä jotain muuta sähköpostipalvelun tiliä, Attractista lähetettävät sähköpostit käyttävät oletusarvoista Microsoftin sähköpostipalvelun tiliä.

## <a name="configure-email-template-settings"></a>Sähköpostimallin asetusten määrittäminen

Voit ladata yrityksen logon kuvan ja muita tietoja sähköpostien brändin mukaiseksi ylätunnisteeksi. Voit myös muodostaa sähköpostin alatunnisteisiin linkkejä tietosuojakäytäntöön ja käyttöehtoihin.

> [!NOTE]
> Sinun on noudatettava sekä kaikkia oman maasi tai alueesi sovellettavia lakeja että sen maan tai alueen lakeja, jotka koskevat sähköpostin vastaanottajaa. Nämä lait sisältävät roskapostisuojaa koskevia säädöksiä.

1. Valitse ensin **Asetukset** (rataskuvake oikeassa yläkulmassa) ja sitten **Hallintakeskus**.
2. Vedä **Sähköpostimallin asetukset** -kohdan **Sähköpostiasetukset**-välilehdessä sähköpostin ylätunnisteena käytettävä kuva kuvaruutuun. Voit myös napsauttaa kuvaruutua ja siirtyä kyseiseen tiedostoon. Voit vaihtaa nykyisen kuva valitsemalla ensin sen vieressä **Poista**. Kuvan on oltava JPEG-, JPG-, PNG- tai SVG-tiedosto. Suositeltu kuvakoko on leveydeltään 25–800 kuvapistettä ja korkeudeltaan 25–150 kuvapistettä. Ylätunnisteen kuvatiedoston enimmäiskoko on 1 megatavu (Mt).

    ![Yrityksen sähköpostin ylätunnisteen kuvan lisääminen](./media/attract-admin-email-header.png)

3. Lisää **Oma tietosuojakäytäntösi viestintää varten** -kohtaan linkki yrityksen tietosuojakäytäntöön. Lisää **Omat käyttöehtosi viestintää varten** -kohtaan linkki yrityksen käyttöohjeisiin.

    ![Yrityksen tietosuojakäytännön ja käyttöehtojen linkin lisääminen sähköpostin alatunnisteeseen](./media/attract-admin-email-footer.png)

4. Tallenna sähköpostimallin asetukset valitsemalla **Tallenna**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]