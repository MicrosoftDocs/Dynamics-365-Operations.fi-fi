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
ms.openlocfilehash: c4d78103a3c08ee4052290fccf6750aba7eecf4a
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474096"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>Versiohistorian näyttäminen sivujen ja osien palauttamista varten

[!include [banner](includes/banner.md)]

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
