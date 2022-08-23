---
title: Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta
description: Tässä artikkelissa selitetään, miten sähköisiä raportointikokoonpanoja ladataan Configuration Service -palvelun yleisestä tietovarastosta.
author: kfend
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
ms.openlocfilehash: 3bbc341d1668e54fcb4034263a7e142166a94b05
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273305"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa selitetään, miten määrityspalvelun yleisestä säilöstä ladataan [sähköisen raportoinnin määrityksiä](general-electronic-reporting.md#Configuration). Lisätietoja on kohdassa [Microsoft Dynamics 365 Finance – Regulatory Services, määrityspalvelu](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Konfiguraatiosäilön avaaminen

1. Kirjaudu Dynamics 365 Finance -sovellukseen yhdellä seuraavista rooleista:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

2. Valitse **Organisaation hallinto > Työtilat > Sähköinen raportointi**.
3. Valitse **Konfiguraation lähteet** -osassa **Microsoft**-ruutu.
3. Valitse **Microsoft**-ruudusta **Säilöt**.

    ![Sähköisen raportoinnin työtila.](./media/er-download-configurations-global-repo-er-workspace.png)

4. Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **Yleinen**. Jos säilöä ei ole ruudukossa, noudata seuraavia ohjeita:

    1. Valitse uusi säilö napsauttamalla **Lisää**-linkkiä.
    2. Valitse varastotyypiksi **Yleinen** ja valitse sitten **Luo säilö**.
    3. Noudata luvananto-ohjeita tarvittaessa.
    4. Kirjoita arkiston nimi ja kuvaus ja vahvista uusi tietovarastokohta valitsemalla **OK**.
    5. Valitse ruudukossa uusi **Yleinen**-tyypin säilö.

5. Valitsemalla **Avaa** voit tarkastella valitun säilön ER-konfiguraatioita.

    ![Konfiguraatiosäilöjen sivu.](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Tuo yksi määritys

1. **Valitse konfigurointisäilöt** -sivun konfiguraatiopuussa haluamasi ER-konfiguraatio.
2. Valitse **Versiot**-pikavälilehdellä valitun ER-konfiguraation tarvittava versio.
3. Lataa valittu versio yleisestä säilöpalvelusta nykyiseen Finance-esiintymään valitsemalla **Tuo**.

    > [!NOTE]
    > **Tuo**-painike ei ole käytettävissä ER-määritysversioille, jotka on jo ladattu nykyiseen Finance-esiintymään.

    ![Konfiguraatiotietovarastosivu, Konfiguroinnit-pikavälilehti.](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Tuo suodatetut määritykset

1. Laajenna **Konfigurointisäilöt** -sivun konfiguraatiot-puussa **Suodatin**-pikavälilehti.
2. Lisää tarvittavat Tunnisteet **Tunnisteet**-ruudukkoon.
3. Valitse **Maa- tai aluesoveltuvuus** -kentästä haluamasi maa-/aluekoodit ja valitse sitten **Käytä suodatinta**.

    > [!NOTE]
    > **Konfiguraatiot**-pikavälilehdessä näkyvät kaikki määritetyt valintaehdot täyttävät konfiguraatiot.

4. Lataa suodatetut konfiguraatiot yleisestä tietovarastosta nykyiseen esiintymään valitsemalla **Konfiguraatiot**-pikavälilehdessä **Tuo**.
5. Voit tyhjentää määritetyt valintaehdot valitsemalla **Konfiguraatiot**-pikavälilehdessä **Nollaa suodatin**.

    ![Konfigurointitietovarastosivu, Versiot-pikavälilehti, Tuo-painike.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> ER-asetusten mukaan määritykset tarkistetaan tuonnin jälkeen. Voit saada ilmoituksia havaituista epäyhtenäisyysongelmista. Ennen kuin voit käyttää tuotua konfiguraatioversiota, kyseiset ongelmat on ratkaistava. Lisätietoja saat tähän artikkeliin liittyvistä resursseista.

> [!NOTE]
> ER-konfiguraatiot voidaan määrittää riippuvaisiksi muista konfiguraatioista. Tämän vuoksi yhdessä valitun konfiguraation kanssa voidaan automaattisesti tuoda muita konfiguraatioita. Lisätietoja määritysten riippuvuuksista on kohdassa [ER-konfiguraatioiden riippuvuuden määrittäminen muissa komponenteissa](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

