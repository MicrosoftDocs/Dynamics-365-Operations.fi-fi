---
title: IoT-analytiikkaskenaarion määrittäminen
description: Tässä ohjeaiheessa käsitellään IoT-analytiikkaskenaarion määrittämistä Supply Chain Managementista.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597165"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT-analytiikkaskenaarion määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään IoT-analytiikkaskenaarion määrittämistä Supply Chain Managementista. Ennen skenaarioiden määrittämistä on [määritettävä LCS](iot-lcs-setup.md).

Tässä ohjeaiheessa määritetään **Laiteseisokki**-skenaario luomaan ilmoitus Supply Chain Managementissa, kun kone sammuu.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>**Laiteseisokki**-skenaarion määrittäminen Supply Chain Managementissa

**Laiteseisokki**-skenaariossa osan lähtevä signaali yhdistetään koneen hälytysrajaan. Konetta valvotaan vain silloin, kun se on valittu skenaarioon ja määritetty suoritettavaksi Supply Chain Managementissa. Jos koneen viimeisestä vastaanotetusta Osa pois käytöstä -signaalista kulunut aika on suurempi kuin hälytysraja, **Kone sammunut** -ilmoitus käynnistetään. Jos kone on edelleen käynnissä, kun seuraava **PartOut**-signaali vastaanotetaan, **Kone käynnissä** -ilmoitus käynnistetään. Jos kone pysyy sammuneena 30 minuuttia, uusi **Kone sammunut** -ilmoitus käynnistetään.

**Laiteseisokki**-skenaariossa on seuraavat riippuvuudet:

+ Tuotantotilauksen on oltava meneillään yhdistetyssä koneessa, jotta hälytys käynnistyy.
+ IoT-keskittimeen lähetettävässä yhdistetyn koneen Osa pois käytöstä -signaalilla on oltava yksilöivä ominaisuuden nimi.
+ IoT-keskittimen sanomassa on oltava Unix-millisekunnin aikaleimaominaisuus.

Skenaario määritetään seuraavasti:

1. Kirjaudu Supply Chain Managementiin.
2. Ota IoT-analytiikkatoiminnon merkintä käyttöön. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Määritä mittarit. Lisätietoja on kohdassa [Mittarien määrittäminen](iot-metrics-setup.md#configure-metrics).
4. Siirry **Tuotannonhallinta**-kohtaan.
5. Valitse **Asetukset \> IoT-analytiikka \> Skenaarionhallinta**.
6. Valitse **Laiteseisokki**-ruudussa **Määritä**. Ohjattu määritystoiminto käynnistyy **Laiteanturin rakennemääritys** -sivulla. Tavoitteena on määrittää Supply Chain Managementissa rakenne, joka vastaa IoT-sanoman JSON-muotoa. Sanomarakenteita voi määrittää useita. Lisätietoja on kohdassa [IoT-keskittimen sanomarakenteen muodot](iot-schema-format.md). Tässä esimerkissä sanoma sisältää seuraavan muotoisen sanomaerän:

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

7. Lisää rivi tauluun.

    1. Määritä **Rakenteen nimi** -arvoksi **ID**.
    2. Määritä **Rakenteen polku** -arvoksi **/payload[\*]/id**.
    3. Määritä **Kuvaus**-arvoksi **Sanoman tunnus**.

8. Lisää rivi tauluun.

    1. Määritä **Rakenteen nimi** -arvoksi **Timestamp**.
    2. Määritä **Rakenteen polku** -arvoksi **/payload[\*]/timestamp**.
    3. Määritä **Kuvaus**-arvoksi **Sanoman aikaleima**.

9. Lisää rivi tauluun.

    1. Määritä **Rakenteen nimi** -arvoksi **Value**.
    2. Määritä **Rakenteen polku** -arvoksi **/payload[\*]/value**.
    3. Määritä **Kuvaus**-arvoksi **Sanoman arvo**.

    Sanoman kaikki ominaisuuksia ei tarvitse määrittää vaan tarvittavien ominaisuuksien määrittäminen riittää. Tässä esimerkissä eri tarvitse luoda **Juuren aikaleima** -riviä. **Juuren aikaleima** -polku olisi **/timestamp**.
  
10. Siirry **Laiteanturin rakenteen yhdistämismääritys** -sivulle valitsemalla **Seuraava**.
11. Määritä **Laitteen resurssitunnus** -rivin **Rakenteen nimi** -arvoksi **ID**. Kelvolliset arvot näkyvät avattavassa taulukossa.
12. Määritä **UTC-aika**-rivin **Rakenteen rivi** -arvoksi **Timestamp**. Kelvolliset arvot näkyvät avattavassa taulukossa.
13. Määritä **Osan tuottama signaali** -rivin **Rakenteen nimi** -arvoksi **Value**. Kelvolliset arvot näkyvät avattavassa taulukossa.
14. Valitse **Laitteen resurssitunnuksen määritys** -sivulla **Seuraava**.
15. Tässä vaiheessa IoT-keskittimen sanoman arvot yhdistetään Supply Chain Managementin resursseihin.

    1. Lisää **Signaalin tietoarvot** -taulussa uusi rivi ja anna **Arvo**-sarakkeessa **IoTInt.Machine1225.PartOut**. Arvo **IoTInt.Machine1225.PartOut** saadaan IoT-keskittimen sanoman JSON **id** -ominaisuudesta.
    2. Valitse **Tallenna**.
    3. Valitse **Liiketoimintatietueen yhdistäminen** -taulussa **Uusi**. **Liiketoimintatietueen tyyppi** -oletusarvo täytetään automaattisesti eikä sitä tarvitse muuttaa.
    4. Valitse **Liiketoimintatietue**-sarakkeessa, se Supply Chain Managementin koneresurssi, josta signaalin arvo lähetetään.
    5. Valitse **Tallenna**.
    6. Lisää koneen **Machine1226** uusi tietueen yhdistämismääritys toistamalla nämä vaiheet. Useita signaalin tietoarvoja voi yhdistää yhteen Supply Chain Managementin tietueeseen.

16. Valitse käsiteltävät koneet **Valitut**-sarakkeen avulla. Kaikkia signaalin arvoja ei tarvitse määrittää eikä kaikkia koneita tarvitse valita.
17. Siirry **Osan tuottaman signaalin määritys** -sivulle valitsemalla **Seuraava**.
18. Lisää **Signaalin tietoarvot** -taulussa uusi rivi, ja valitse **Arvo**-asetukseksi **Tosi**. Arvo **Tosi** saadaan IoT-keskittimen sanoman JSON **value** -ominaisuudesta. Voit lisätä skenaarioon tarvittavan määrän arvoja.
19. Valitse **Tallenna**.
20. Siirry **Laiteseisokin raja-arvo** -sivulle valitsemalla **Seuraava**. Luettelossa olevat koneet on yhdistetty aiemmin signaalin arvoihin. Tässä vaiheessa määritettävä raja-arvo määrittää, onko kone sammunut. Jos raja-arvoksi määritetään esimerkiksi 10. Supply Chain Management luo ilmoituksen, jos kone ei lähetä osa pois käytöstä -sanomaa 10 minuuttiin.
21. Siirry **Ota skenaario käyttöön** -sivulle valitsemalla **Seuraava**. Ota skenaario käyttöön siirtämällä liukusäädintä.
22. Valitse **Valmis**.

Skenaario on nyt määritetty. IoT-analytiikka aloittaa automaattisesti IoT-keskittimen sanomien käsittelyn.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>**Tuotteen laatu** -skenaarion määrittäminen Supply Chain Managementissa

**Tuotteen laatu** -skenaario luo ilmoituksen, jos nimikkeen määrite on määritetyn alueen ulkopuolella. Anturi voi esimerkiksi lähettää kunkin nimikkeen painon IoT-keskittimeen. Ilmoitus luodaan Supply Chain Managementissa, jos nimike oli liian raskas tai liian kevyt.

Skenaariossa on seuraavat riippuvuudet:

+ Tuotantotilauksen on oltava käynnissä yhdistetyssä koneessa ja valmistamassa tuotetta, jossa on yhdistetty erämäärite, jotta hälytys käynnistyy.
+ IoT-keskittimeen lähetettävässä erämääritteen ilmaisevalla signaalilla on oltava yksilöivä ominaisuuden nimi.
+ IoT-keskittimen sanomassa on oltava Unix-millisekunnin aikaleimaominaisuus.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>**Tuotannon viivästykset** -skenaarion määrittäminen Supply Chain Managementissa

**Tuotannon viivästykset** -skenaario luo ilmoituksen, jos tuotantokapasiteetti alittaa raja-arvon. Tässä skenaariossa kunkin tuotetun nimikkeen **PartOut**-signaali lähetetään IoT-keskittimeen. Tilauksen viivästyminen lasketaan Supply Chain Managementissa sen perusteella, kuinka pitkäksi tuotantotilauksen suorittaminen ajoitettu, kuinka monta nimikettä tuotetaan, kuinka kauan työ on ollut meneillään ja kuinka monta **PartOut**-signaalia vastaanotetaan. Viivästysilmoitus luodaan, jos työn **PartOut**-signaalien määrä alittaa odotetun arvon raja-arvon.

Skenaariossa on seuraavat riippuvuudet:

+ Tuotantotilauksen on oltava meneillään yhdistetyssä koneessa, jotta hälytys käynnistyy.
+ IoT-keskittimeen lähetettävässä yhdistetyn koneen Osa pois käytöstä -signaalilla on oltava yksilöivä ominaisuuden nimi.
+ IoT-keskittimen sanomassa on oltava Unix-millisekunnin aikaleimaominaisuus.

## <a name="how-to-disable-a-scenario"></a>Skenaarion poistaminen käytöstä

Skenaario poistetaan käytöstä seuraavasti:

1. Valitse Supply Chain Managementissa **Tuotannonhallinta \> Asetukset \> IoT-analytiikka \> Skenaarionhallinta**.
2. Valitse skenaariossa **Määritys**.
3. Siirry ohjatun toiminnon viimeiseen välilehteen valitsemalla **Seuraava**.
4. Poista skenaario käytöstä siirtämällä liukusäädintä.
