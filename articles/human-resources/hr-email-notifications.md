---
title: Edut-sähköposti-ilmoitus
description: Tässä artikkelissa on yhteenveto Microsoft Dynamics 365 Human Resourcesin Etujen hallinnan sähköposti-ilmoitusominaisuudesta.
author: twheeloc
ms.date: 08/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d550cbb2f639535dbb43765c9fb0632a514fbe8c
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229912"
---
# <a name="benefits-email-notification"></a>Edut-sähköposti-ilmoitus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

Sähköposti-ilmoitustoiminnon avulla sähköposti-ilmoitukset ja muistutukset voidaan lähettää työntekijöille seuraavissa tilanteissa:

- Uuden työntekijän rekisteröinti
- Avaa rekisteröinti
- Elämäntapahtumien kelpoisuus

Voit luoda ja määrittää useita sähköpostimalleja sekä lähettää ilmoitukset Käyttämällä **Etujen hallinta** -työtilaa ja **Työsuhde-edut** -sivua. Voit myös seurata ilmoitusten/muistutusten historiatietoja.

## <a name="set-up-human-resources-shared-parameters"></a>Määritä jaetut henkilöstöparametrit

**Henkilöstöhallinnon jaetut parametrit** -sivulla voit luoda etusähköpostimalleja erilaisille työntekijöille tai työntekijäryhmille lähetetyille viestintätyypeille.

## <a name="create-a-new-email-id-template"></a>Uuden sähköpostitunnusmallin luominen

Voit luoda uuden sähköpostitunnusmallin seuraavien ohjeiden avulla.

1. Valitse **Järjestelmän sähköpostimallit**.
2. Valitse **Uusi**.
3. Kirjoita **Sähköpostitunnus**-kenttään nimi.
4. Määritä muut kentät tarpeen mukaan.
5. Lataa malli valitsemalla **Sähköpostiviesti**.
6. Valitse **Henkilöstöhallinnon jaetut parametrit** -sivulla uusi malli **Järjestelmämallit**-kohdasta ja siirrä se **Etuihin liittyvät mallit** -kohtaan.

## <a name="send-email-to-employees"></a>Lähetä sähköpostiviesti työntekijöille

Noudattamalla seuraavia ohjeita voit lähettää sähköpostiviestin uudelle työntekijälle, joka ei ole vielä aloittanut.

1. Avaa **Etujen hallinta** -työtila.
2. Valitse sen työntekijäryhmän ruutu, jolle haluat lähettää sähköpostiviestin.
3. Valitse **Lähetä sähköpostiviesti**.
4. Valitse työntekijät, joille haluat lähettää sähköpostin.
5. Valitse **Lähetä sähköpostiviesti**.
6. Valitse malli, jota haluat käyttää.
7. Lähetä sähköposti valitsemalla **OK**.

    Voit tarkistaa sähköpostiviestin ja tilan työntekijän **Työsuhde-edut**-sivulta tai valitsemalla **Etujen sähköpostihistoria** **Etujen hallinta** -työtilan **Linkit**-osasta. Voit lähettää sähköpostiviestin myös **Työntekijän etusuunnitelma** -sivulta.

8. Voit tarkastella etujen sähköpostihistoriaa **Etujen hallinta** -työtilan **Linkit**-osassa **Etujen sähköpostihistoria**.
9. Tarkastele lähetettyjen etujen sähköpostien täydellistä sähköpostihistoriaa. Voit tarkistaa sähköpostiviestin sisällön valitsemalla **Näytä sanoma**.
10. Valitse **Työntekijä**.
11. Voit lähettää sähköpostiviestin ja tarkastella etujen sähköpostihistoriaa **Työntekijän etusuunnitelma** -sivulla.

**Etujen hallinta** -työtilassa on erilaisia ruutuja. Voit lähettää sähköpostiviestejä valitsemalla liittyvän mallin. Jos uuden työntekijän rekisteröintisähköpostit on lähetetty, **Uusi työntekijä, ei aloitettu** -ruutu ja valitse sitten **Lähetä muistutus** -linkki. Voit valita muistutusmallin ja määrittää ilmoituksen otsikoksi ensimmäisen, toisen tai kolmannen muistutuksen.
