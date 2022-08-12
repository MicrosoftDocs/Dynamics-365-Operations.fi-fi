---
title: Versiohistorian näyttäminen sivujen ja osien palauttamista varten
description: Tässä artikkelissa käsitellään sivun tai osan versiohistorian näyttämistä ja palauttamista aiempaan versioon Microsoft Dynamics 365 Commercen sivustonmuodostimessa.
author: phinneyridge
ms.date: 06/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: fa2ecdd9d9bc7e60b279d850573b5caa6df2c659
ms.sourcegitcommit: 9cfccb5c260ce56a3457f9ea12e80f54ea55a3b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183673"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>Versiohistorian näyttäminen sivujen ja osien palauttamista varten

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä artikkelissa käsitellään sivun tai osan versiohistorian näyttämistä ja palauttamista aiempaan versioon Microsoft Dynamics 365 Commercen sivustonmuodostimessa.

Commercen sivustonmuodostimessa voidaan tarkastella sivun tai osan versiohistoriaa ja palauttaa asiakirja tarvittaessa tiettyyn versioon. Avoimessa asiakirjassa voidaan valita komentopalkissa **Näytä historia**, joka avaa **Versiohistoria**-valintaikkunan. Tämän valintaikkunan **Versio**-välilehdessä on luettelo sivun tai osan kaikkien versioiden ja tallennusaktiviteettien historiatiedoista. Sitten voidaan valita luettelossa olevan asiakirjan edellinen versio, esikatsella se ja palauttaa sen nykyiseksi versioksi. Valintaikkunan **Aktiviteetti**-välilehdessä on asiakirjan täydellisen aktiviteettihistorian sisältävä luettelo, ja siinä on mukana kaikki tallennus-, julkaisu- ja julkaisun peruutustoiminnot.

> [!NOTE]
> Asiakirjasta luodaan uusi versio aina, kun sivuston tekijä tekee muutoksia ja valitsee sitten asiakirjassa **Muokkaus on valmis**. 

Sivun tai osan versiohistoriaa voidaan tarkastella ja edellinen versio palauttaa seuraavasti.

1. Avaa sivustonmuodostimessa sivu tai osa, jonka versiohistoriaa halutaan tarkastella.
1. Valitse komentopalkissa **Näytä historia**.

    ![Näytä historia -painike](./media/version-history-1.png)

1. Valitse **Versiohistoria**-valintaikkunan **Versio**-välilehdessä asiakirjan edellinen versio. Oikealla olevassa ominaisuusruudussa on valitun version pikkukuva sekä tietoja sen muokkaajasta ja muokkausajankohdasta.

    ![Versiohistorian luettelonäkymä](./media/version-history-2.png)

1. Valitun asiakirjaversion kokonaisena hahmonnettuna esikatselua voi tarkastella valitsemalla **Esikatselu**. Sulje esikatselu ja palaa **Versiohistoria**-valintaikkunaan valitsemalla **Lopeta esikatselu**.
1. Palauta asiakirjan edellinen versio valitsemalla se luettelossa **Versio**-välilehdessä ja valitsemalla sitten **Palauta**. **Palauta versio \<version number\>** -sanomaruutu avautuu, ja siinä pyydetään vahvistamaan palautustoiminto. 

    ![Palautuspainike ja vahvistussanomaruutu](./media/version-history-3.png)

1. Jatka palautustoimintoa valitsemalla **Palauta**. Sivustonmuodostin päivitetään, ja siinä näkyy sivun tai osan palautettu versio.
1. Julkaisu palautettu versio valitsemalla **Lopeta muokkaus** ja valitse sitten **Julkaise**.
