---
title: IoT-analytiikkaskenaarion määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten IoT-analytiikan skenaarioita voidaan määrittää Microsoft Dynamics 365 Supply Chain Managementissa.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d1deaa2130b63272da39a42315c6a1bc4b7ccb8a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427323"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT-analytiikkaskenaarion määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten IoT-analytiikan skenaarioita voidaan määrittää Microsoft Dynamics 365 Supply Chain Managementissa. Ennen kuin voit määrittää skenaarioita, sinun on [Määritettävä Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).

Tässä ohjeaiheessa määritetään **Laiteseisokki**-skenaario siten, että Supply Chain Managementissa luodaan ilmoitus, kun kone sammuu. Tässä kerrotaan myös, miten **Tuotteen laatu** -skenaario määritetään siten, että järjestelmä luo ilmoituksen, jos nimikkeen määrite on määritetyn alueen ulkopuolella, ja miten **Tuotantoviiveet**-skenaario määritetään siten, että järjestelmä luo ilmoituksen, jos tuotantomäärä alittaa raja-arvon.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Laiteseisokki-skenaarion määrittäminen Supply Chain Managementissa

**Laiteseisokki**-skenaariossa **PartOut**-signaali yhdistetään koneen hälytysrajaan. Konetta valvotaan vain silloin, kun se on valittu skenaarioon ja määritetty **Käynnissä**-tilaan Supply Chain Managementissa. Jos koneen viimeisestä koneelta vastaanotetusta **PartOut** -signaalista kulunut aika on suurempi kuin hälytysraja, **Kone sammunut** -ilmoitus käynnistetään. Jos kone on edelleen käynnissä, **Kone käynnissä** -ilmoitus luodaan, kun seuraava **PartOut**-signaali vastaanotetaan. Jos kone pysyy sammuneena 30 minuuttia, luodaan uusi **Kone sammunut** -ilmoitus.

**Laiteseisokki**-skenaariossa on seuraavat riippuvuudet:

+ Hälytys luodaan vain, jos tuotantotilaus on meneillään yhdistetyssä koneessa.
+ Yhdistetyn koneen **PartOut**-signaalia vastaava signaali on lähetettävä IoT-keskittimeen, ja signaalilla on oltava yksilöivä ominaisuuden nimi.
+ Azuren IoT-keskittemen sanomassa on oltava UNIX-**aikaleima**-ominaisuus, jossa arvo ilmaistaan millisekunteina (ms).

Skenaario määritetään seuraavasti.

1. Kirjaudu Supply Chain Managementiin.
2. Ota IoT-analytiikkatoiminnon merkintä käyttöön. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
3. Määritä mittarit. Lisätietoja on kohdassa [Mittarien määrittäminen](iot-metrics-setup.md#configure-metrics).
4. Siirry kohtaan **Tuotannonhallinta \> Määritys \> IoT-analytiikka \> Skenaarionhallinta**.
6. Valitse **Laiteseisokki**-ruudussa **Määritä** avataksesi ohjatun määritystoiminnon.

   Ohjatun määritystoiminnon ensimmäinen sivu on **Laiteanturin rakennemääritys**. Tällä sivulla sinun tavoitteenasi on määrittää rakenne Supply Chain Managementissa siten, että se vastaa IoT-keskittimen sanomien JavaScript Object Notation (JSON) -muotoa. Sanomarakenteita voi määrittää useita. Lisätietoja on kohdassa [Rakennemuodot IoT-keskitinsanomille](iot-schema-format.md). Tässä esimerkissä sanoma sisältää seuraavan muotoisen sanomaerän:

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Lisää rivi taulukkoon ja määritä seuraavat arvot:

    1. Määritä **Rakenteen nimi** -kentän arvoksi **ID**.
    2. Määritä **Rakenteen polku** -kentän arvoksi **/payload\[\*\]/id**.
    3. Määritä **Kuvaus**-kentän arvoksi **Sanoman tunnus**.

8. Lisää uusi rivi taulukkoon ja määritä seuraavat arvot:

    1. Määritä **Rakenteen nimi** -kentän arvoksi **Timestamp**.
    2. Määritä **Rakenteen polku** -kentän arvoksi **/payload\[\*\]/timestamp**.
    3. Määritä **Kuvaus**-kentän arvoksi **Sanoman aikaleima**.

9. Lisää uusi rivi taulukkoon ja määritä seuraavat arvot:

    1. Määritä **Rakenteen nimi** -kentän arvoksi **Arvo**.
    2. Määritä **Rakenteen polku** -kentän arvoksi **/payload\[\*\]/arvo**.
    3. Määritä **Kuvaus**-kentän arvoksi **Sanoman arvo**.

    > [!NOTE]
    > Kaikkia sanoman ominaisuuksia ei tarvitse määrittää. Määritä vain ominaisuudet, joita tarvitset. Edellisissä vaiheissa et luonut riviä **Juuren aikaleima**. **Juuren aikaleima** -polku olisi **/timestamp**.

10. Siirry **Laiteanturin rakenteen yhdistämismääritys** -sivulle valitsemalla **Seuraava**.
11. Määritä **Laitteen resurssitunnus** -rivin **Rakenteen nimi** -kentän arvoksi **ID**.
12. Määritä **UTC-aika**-rivin **Rakenteen rivi** -kentän arvoksi **Timestamp**.
13. Määritä **Osan tuottama signaali** -rivin **Rakenteen nimi** -kentän arvoksi **Arvo**.
14. Siirry **Laitteen resurssitunnuksen määritys** -sivulle valitsemalla **Seuraava**.
15. Näiden ohjeiden avulla IoT-keskittimen sanoman arvot yhdistetään Supply Chain Managementin resursseihin:

    1. Lisää uusi rivi **Signaalitietoarvot**-taulukkoon. Syötä **Arvo**-kenttään **IoTInt.Machine1225.PartOut**. Tämä arvo saadaan IoT-keskittimen sanoman JSON **id** -ominaisuudesta.
    2. Valitse **Tallenna**.
    3. Valitse **Liiketoimintatietueen yhdistäminen** -taulussa **Uusi**. Kentälle **Liiketoimintatietueen tyyppi** täytetään automaattisesti oletusarvo, eikä sitä tarvitse muuttaa.
    4. Valitse **Liiketoimintatietue**-kentässä, se Supply Chain Managementin koneresurssi, josta signaalin arvo lähetetään.
    5. Valitse **Tallenna**.
    6. Lisää koneen **Machine1226** uusi tietueen yhdistämismääritys toistamalla nämä vaiheet. Useita signaalin tietoarvoja voi yhdistää yhteen Supply Chain Managementin tietueeseen.

16. Valitse käsiteltävät koneet **Valitut**-sarakkeen avulla. Kaikkia signaalin arvoja ei tarvitse määrittää eikä kaikkia koneita tarvitse valita.
17. Siirry **Osan tuottaman signaalin määritys** -sivulle valitsemalla **Seuraava**.
18. Lisää **Signaalin tietoarvot** -taulussa uusi rivi, ja määritä **Arvo**-kentän arvoksi **Tosi**. Tämä arvo saadaan IoT-keskittimen sanoman JSON **value** -ominaisuudesta. Voit lisätä skenaarioon tarvittavan määrän arvoja.
19. Valitse **Tallenna**.
20. Siirry **Laiteseisokin raja-arvo** -sivulle valitsemalla **Seuraava**. Luettelossa olevat koneet on yhdistetty aiemmin signaalin arvoihin. Tällä sivulla määritetään raja-arvo määrittämään, onko kone sammunut. Jos raja-arvoksi määritetään esimerkiksi **10**, Supply Chain Management luo ilmoituksen, jos koneelta ei saada **PartOut** -signaalia 10 minuuttiin.
21. Siirry **Ota skenaario käyttöön** -sivulle valitsemalla **Seuraava**. Ota skenaario käyttöön määrittämällä asetus.
22. Valitse **Valmis**.

Skenaarion määritys on nyt valmis. IoT-analytiikka aloittaa automaattisesti IoT-keskittimen sanomien käsittelyn.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Tuotteen laatu -skenaarion määrittäminen Supply Chain Managementissa

**Tuotteen laatu** -skenaario luo ilmoituksen, jos nimikkeen määrite on määritetyn alueen ulkopuolella. Anturi voi esimerkiksi lähettää kunkin nimikkeen painon IoT-keskittimeen. Jos jokin nimike on liian painava tai kevyt Supply Chain Managementissa luodaan ilmoitus.

**Tuotteen laatu** -skenaariossa on seuraavat riippuvuudet:

+ Hälytys voi käynnistyä vain, jos tuotantotilaus on käynnissä yhdistetyssä koneessa ja valmistamassa tuotetta, jossa on yhdistetty erämäärite.
+ IoT-keskittimeen lähetettävässä erämääritteen ilmaisevalla signaalilla on oltava yksilöivä ominaisuuden nimi.
+ IoT-keskittemen sanomassa on oltava UNIX-**aikaleima**-ominaisuus, jossa arvo ilmaistaan millisekunteina (ms).

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Tuotannon viivästykset -skenaarion määrittäminen Supply Chain Managementissa

**Tuotannon viivästykset** -skenaario luo ilmoituksen, jos tuotantokapasiteetti alittaa raja-arvon. Tässä skenaariossa kunkin tuotetun nimikkeen **PartOut**-signaali lähetetään IoT-keskittimeen. Supply Chain Managementissa tilausviive lasketaan sen ajan perusteella, joka tuotantotilausta on tarkoitus suorittaa, tuotettavien nimikkeiden määrän perusteella, tehtävän käynnissäoloajan perusteella sekä vastaanotettujen **PartOut**-signaalien perusteella. Viivästysilmoitus luodaan, jos työn **PartOut**-signaalien määrä alittaa raja-arvon.

**Tuotantoviiveet** -skenaariossa on seuraavat riippuvuudet:

+ Hälytys luodaan vain, jos tuotantotilaus on meneillään yhdistetyssä koneessa.
+ Yhdistetyn koneen **PartOut**-signaalia vastaava signaali on lähetettävä Azuren IoT-keskittimeen, ja signaalilla on oltava yksilöivä ominaisuuden nimi.
+ IoT-keskittemen sanomassa on oltava UNIX-**aikaleima**-ominaisuus, jossa arvo ilmaistaan millisekunteina (ms).

## <a name="disable-a-scenario"></a>Skenaarion poistaminen käytöstä

Skenaario poistetaan käytöstä seuraavasti.

1. Siirry Supply Chain Managementissa kohtaan **Tuotannonhallinta \> Asetukset \> IoT-analytiikka \> Skenaarionhallinta**.
2. Valitse skenaarion ruudussa **Määritä**.
3. Siirry ohjatun toiminnon viimeiselle sivulle valitsemalla **Seuraava**.
4. Poista skenaario käytöstä määrittämällä asetus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]