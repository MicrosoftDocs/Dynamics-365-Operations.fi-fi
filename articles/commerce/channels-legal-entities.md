---
title: Luo oikeushenkilöt
description: Tässä artikkelissa käsitellään yritysten luontia Microsoft Dynamics 365 Commercessa, sillä yritykset on luotava ja määritettävä ennen kanavien luontia.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e99536d3706c842d69060136f23508208b16b461
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276316"
---
# <a name="create-legal-entities"></a>Luo oikeushenkilöt

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään yritysten luontia Microsoft Dynamics 365 Commercessa, sillä yritykset on luotava ja määritettävä ennen kanavien luontia.

Yritys on organisaatio, jolla on rekisteröity tai lain vaatima rakenne. Yritys voi solmia oikeudellisia sopimuksia ja yritykseltä edellytetään suorituskykyä kuvaavien lausuntojen valmistelemista.

Yritys on tietyntyyppinen oikeushenkilö Tällä hetkellä yritykset ovat ainoita luotavia oikeushenkilöitä ja jokainen oikeushenkilö on liitetty yritystunnukseen. Tämä liitos on olemassa, koska ohjelman eräät toiminnalliset alueet käyttävät yritystunnusta tai *DataAreaId*-tunnusta tietomalleissaan. Näillä toiminnallisilla alueilla yrityksiä käytetään tietoturvan rajana. Käyttäjillä on pääsy vain sen yrityksen tietoihin, jonka järjestelmään he ovat sillä hetkellä kirjautuneena. 

Kanavaa luotaessa on määritettävä, mihin yritykseen kanava kuuluu.

## <a name="create-a-new-legal-entity"></a>Uuden yrityksen luominen

Luo uusi yritys Dynamics 365 Commercessa seuraavien ohjeiden mukaisesti.

1. Valitse siirtymisruudussa **Moduulit \> Pääkonttorin asetukset \> Yritykset**.
1. Valitse toimintoruudussa **Uusi**. Oikealle tulee **Uusi yritys** -ruutu.
1. Anna **Nimi**-kenttään arvo.
1. Kirjoita arvo **Yritys**-kenttään.
1. Syötä tai valitse arvo **Maa/alue**-kentässä.
1. Valitse **OK**. 

   ![Yrityksen luominen.](media/legal-entities.png)

1. Anna **Yleiset**-osassa seuraavat yleistiedot yrityksestä: 
   1. Kirjoita hakunimi, jos hakunimi on pakollinen. Hakunimi on vaihtoehtoinen nimi, jota voidaan käyttää tämän yrityksen etsimiseen. 
   1. Valitse käytetäänkö tätä oikeushenkilöä konsolidointiyrityksenä.
   1. Valitse käytetäänkö tätä oikeushenkilöä eliminointiyrityksenä. 
   1. Valitse entiteetin **oletuskieli**. 
   1. Valitse entiteetin **aikavyöhyke**.
1. Valitse **Osoitteet**-osassa **Muokkaa** ja anna osoitetiedot, kuten kadun nimi ja numero sekä postinumero ja postitoimipaikka.
1. Kirjoita **Yhteystiedot**-osaan tiedot viestintämenetelmistä, kuten sähköpostiosoitteet, URL-osoitteet ja puhelinnumerot.
1. Kirjoita **Lakisääteinen raportointi** -osaan rekisterinumerot, joita käytetään lakisääteisiin ilmoituksiin.
1. Kirjoita **Rekisteröintinumerot**-osaan kaikki yrityksestä vaadittavat tiedot.
1. Kirjoita **Pankkitilin tiedot** -osaan yrityksen pankkitilien numerot ja reititysnumerot.
1. Kirjoita **Ulkomaankauppa ja -logistiikka** osaan yrityksen lähetystiedot.
1. **Numerosarjat**-osassa voit tarkastella yritykseen liitettyjä numerosarjoja. Tämä on aluksi tyhjä.
1. **Koontinäytön kuva** -osassa voit tarkastella yritykseen liitettyä logoa ja koontinäytön kuvaa sekä vaihtaa sen.
1. Kirjoita **Verorekisteröinti**-osaan rekisterinumerot, joita käytetään raportoitaessa veroviranomaisille.
1. Kirjoita **Vero 1099** -osaan yrityksen 1099-tiedot.
1. Anna yrityksen verotiedot **Verotiedot**-osaan.
1. Valitse **Tallenna**.

Seuraavassa kuvassa näkyy esimerkkiyrityksen tiedot.

![Yrityksen yleinen osa.](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Lisäresurssit

[Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisaatiohierarkian suunnitteleminen](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisaatiohierarkiat](channels-org-hierarchies.md)

[Kanavien yleiskatsaus](channels-overview.md)

[Kanava-asetusten edellytykset](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
