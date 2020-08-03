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
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="ae201-103">IoT-analytiikkaskenaarion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ae201-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae201-104">Tässä ohjeaiheessa käsitellään IoT-analytiikkaskenaarion määrittämistä Supply Chain Managementista.</span><span class="sxs-lookup"><span data-stu-id="ae201-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="ae201-105">Ennen skenaarioiden määrittämistä on [määritettävä LCS](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ae201-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="ae201-106">Tässä ohjeaiheessa määritetään **Laiteseisokki**-skenaario luomaan ilmoitus Supply Chain Managementissa, kun kone sammuu.</span><span class="sxs-lookup"><span data-stu-id="ae201-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="ae201-107">**Laiteseisokki**-skenaarion määrittäminen Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="ae201-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="ae201-108">**Laiteseisokki**-skenaariossa osan lähtevä signaali yhdistetään koneen hälytysrajaan.</span><span class="sxs-lookup"><span data-stu-id="ae201-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="ae201-109">Konetta valvotaan vain silloin, kun se on valittu skenaarioon ja määritetty suoritettavaksi Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="ae201-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="ae201-110">Jos koneen viimeisestä vastaanotetusta Osa pois käytöstä -signaalista kulunut aika on suurempi kuin hälytysraja, **Kone sammunut** -ilmoitus käynnistetään.</span><span class="sxs-lookup"><span data-stu-id="ae201-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="ae201-111">Jos kone on edelleen käynnissä, kun seuraava **PartOut**-signaali vastaanotetaan, **Kone käynnissä** -ilmoitus käynnistetään.</span><span class="sxs-lookup"><span data-stu-id="ae201-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="ae201-112">Jos kone pysyy sammuneena 30 minuuttia, uusi **Kone sammunut** -ilmoitus käynnistetään.</span><span class="sxs-lookup"><span data-stu-id="ae201-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="ae201-113">**Laiteseisokki**-skenaariossa on seuraavat riippuvuudet:</span><span class="sxs-lookup"><span data-stu-id="ae201-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="ae201-114">Tuotantotilauksen on oltava meneillään yhdistetyssä koneessa, jotta hälytys käynnistyy.</span><span class="sxs-lookup"><span data-stu-id="ae201-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="ae201-115">IoT-keskittimeen lähetettävässä yhdistetyn koneen Osa pois käytöstä -signaalilla on oltava yksilöivä ominaisuuden nimi.</span><span class="sxs-lookup"><span data-stu-id="ae201-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="ae201-116">IoT-keskittimen sanomassa on oltava Unix-millisekunnin aikaleimaominaisuus.</span><span class="sxs-lookup"><span data-stu-id="ae201-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="ae201-117">Skenaario määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ae201-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="ae201-118">Kirjaudu Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="ae201-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="ae201-119">Ota IoT-analytiikkatoiminnon merkintä käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ae201-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="ae201-120">Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ae201-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="ae201-121">Määritä mittarit.</span><span class="sxs-lookup"><span data-stu-id="ae201-121">Configure the metrics.</span></span> <span data-ttu-id="ae201-122">Lisätietoja on kohdassa [Mittarien määrittäminen](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="ae201-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="ae201-123">Siirry **Tuotannonhallinta**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="ae201-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="ae201-124">Valitse **Asetukset \> IoT-analytiikka \> Skenaarionhallinta**.</span><span class="sxs-lookup"><span data-stu-id="ae201-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="ae201-125">Valitse **Laiteseisokki**-ruudussa **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="ae201-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="ae201-126">Ohjattu määritystoiminto käynnistyy **Laiteanturin rakennemääritys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ae201-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="ae201-127">Tavoitteena on määrittää Supply Chain Managementissa rakenne, joka vastaa IoT-sanoman JSON-muotoa.</span><span class="sxs-lookup"><span data-stu-id="ae201-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="ae201-128">Sanomarakenteita voi määrittää useita.</span><span class="sxs-lookup"><span data-stu-id="ae201-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="ae201-129">Lisätietoja on kohdassa [IoT-keskittimen sanomarakenteen muodot](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="ae201-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="ae201-130">Tässä esimerkissä sanoma sisältää seuraavan muotoisen sanomaerän:</span><span class="sxs-lookup"><span data-stu-id="ae201-130">In this example, the message payload contains a batch of messages with this format:</span></span>

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

7. <span data-ttu-id="ae201-131">Lisää rivi tauluun.</span><span class="sxs-lookup"><span data-stu-id="ae201-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="ae201-132">Määritä **Rakenteen nimi** -arvoksi **ID**.</span><span class="sxs-lookup"><span data-stu-id="ae201-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="ae201-133">Määritä **Rakenteen polku** -arvoksi **/payload[\*]/id**.</span><span class="sxs-lookup"><span data-stu-id="ae201-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="ae201-134">Määritä **Kuvaus**-arvoksi **Sanoman tunnus**.</span><span class="sxs-lookup"><span data-stu-id="ae201-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="ae201-135">Lisää rivi tauluun.</span><span class="sxs-lookup"><span data-stu-id="ae201-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="ae201-136">Määritä **Rakenteen nimi** -arvoksi **Timestamp**.</span><span class="sxs-lookup"><span data-stu-id="ae201-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="ae201-137">Määritä **Rakenteen polku** -arvoksi **/payload[\*]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="ae201-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="ae201-138">Määritä **Kuvaus**-arvoksi **Sanoman aikaleima**.</span><span class="sxs-lookup"><span data-stu-id="ae201-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="ae201-139">Lisää rivi tauluun.</span><span class="sxs-lookup"><span data-stu-id="ae201-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="ae201-140">Määritä **Rakenteen nimi** -arvoksi **Value**.</span><span class="sxs-lookup"><span data-stu-id="ae201-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="ae201-141">Määritä **Rakenteen polku** -arvoksi **/payload[\*]/value**.</span><span class="sxs-lookup"><span data-stu-id="ae201-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="ae201-142">Määritä **Kuvaus**-arvoksi **Sanoman arvo**.</span><span class="sxs-lookup"><span data-stu-id="ae201-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="ae201-143">Sanoman kaikki ominaisuuksia ei tarvitse määrittää vaan tarvittavien ominaisuuksien määrittäminen riittää.</span><span class="sxs-lookup"><span data-stu-id="ae201-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="ae201-144">Tässä esimerkissä eri tarvitse luoda **Juuren aikaleima** -riviä.</span><span class="sxs-lookup"><span data-stu-id="ae201-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="ae201-145">**Juuren aikaleima** -polku olisi **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="ae201-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="ae201-146">Siirry **Laiteanturin rakenteen yhdistämismääritys** -sivulle valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="ae201-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="ae201-147">Määritä **Laitteen resurssitunnus** -rivin **Rakenteen nimi** -arvoksi **ID**.</span><span class="sxs-lookup"><span data-stu-id="ae201-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="ae201-148">Kelvolliset arvot näkyvät avattavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="ae201-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="ae201-149">Määritä **UTC-aika**-rivin **Rakenteen rivi** -arvoksi **Timestamp**.</span><span class="sxs-lookup"><span data-stu-id="ae201-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="ae201-150">Kelvolliset arvot näkyvät avattavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="ae201-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="ae201-151">Määritä **Osan tuottama signaali** -rivin **Rakenteen nimi** -arvoksi **Value**.</span><span class="sxs-lookup"><span data-stu-id="ae201-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="ae201-152">Kelvolliset arvot näkyvät avattavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="ae201-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="ae201-153">Valitse **Laitteen resurssitunnuksen määritys** -sivulla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="ae201-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="ae201-154">Tässä vaiheessa IoT-keskittimen sanoman arvot yhdistetään Supply Chain Managementin resursseihin.</span><span class="sxs-lookup"><span data-stu-id="ae201-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="ae201-155">Lisää **Signaalin tietoarvot** -taulussa uusi rivi ja anna **Arvo**-sarakkeessa **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="ae201-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="ae201-156">Arvo **IoTInt.Machine1225.PartOut** saadaan IoT-keskittimen sanoman JSON **id** -ominaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="ae201-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="ae201-157">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ae201-157">Click **Save**.</span></span>
    3. <span data-ttu-id="ae201-158">Valitse **Liiketoimintatietueen yhdistäminen** -taulussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ae201-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="ae201-159">**Liiketoimintatietueen tyyppi** -oletusarvo täytetään automaattisesti eikä sitä tarvitse muuttaa.</span><span class="sxs-lookup"><span data-stu-id="ae201-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="ae201-160">Valitse **Liiketoimintatietue**-sarakkeessa, se Supply Chain Managementin koneresurssi, josta signaalin arvo lähetetään.</span><span class="sxs-lookup"><span data-stu-id="ae201-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="ae201-161">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ae201-161">Click **Save**.</span></span>
    6. <span data-ttu-id="ae201-162">Lisää koneen **Machine1226** uusi tietueen yhdistämismääritys toistamalla nämä vaiheet.</span><span class="sxs-lookup"><span data-stu-id="ae201-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="ae201-163">Useita signaalin tietoarvoja voi yhdistää yhteen Supply Chain Managementin tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="ae201-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="ae201-164">Valitse käsiteltävät koneet **Valitut**-sarakkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="ae201-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="ae201-165">Kaikkia signaalin arvoja ei tarvitse määrittää eikä kaikkia koneita tarvitse valita.</span><span class="sxs-lookup"><span data-stu-id="ae201-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="ae201-166">Siirry **Osan tuottaman signaalin määritys** -sivulle valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="ae201-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="ae201-167">Lisää **Signaalin tietoarvot** -taulussa uusi rivi, ja valitse **Arvo**-asetukseksi **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="ae201-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="ae201-168">Arvo **Tosi** saadaan IoT-keskittimen sanoman JSON **value** -ominaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="ae201-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="ae201-169">Voit lisätä skenaarioon tarvittavan määrän arvoja.</span><span class="sxs-lookup"><span data-stu-id="ae201-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="ae201-170">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ae201-170">Click **Save**.</span></span>
20. <span data-ttu-id="ae201-171">Siirry **Laiteseisokin raja-arvo** -sivulle valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="ae201-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="ae201-172">Luettelossa olevat koneet on yhdistetty aiemmin signaalin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="ae201-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="ae201-173">Tässä vaiheessa määritettävä raja-arvo määrittää, onko kone sammunut.</span><span class="sxs-lookup"><span data-stu-id="ae201-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="ae201-174">Jos raja-arvoksi määritetään esimerkiksi 10. Supply Chain Management luo ilmoituksen, jos kone ei lähetä osa pois käytöstä -sanomaa 10 minuuttiin.</span><span class="sxs-lookup"><span data-stu-id="ae201-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="ae201-175">Siirry **Ota skenaario käyttöön** -sivulle valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="ae201-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="ae201-176">Ota skenaario käyttöön siirtämällä liukusäädintä.</span><span class="sxs-lookup"><span data-stu-id="ae201-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="ae201-177">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ae201-177">Click **Finish**.</span></span>

<span data-ttu-id="ae201-178">Skenaario on nyt määritetty.</span><span class="sxs-lookup"><span data-stu-id="ae201-178">The scenario setup is complete.</span></span> <span data-ttu-id="ae201-179">IoT-analytiikka aloittaa automaattisesti IoT-keskittimen sanomien käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="ae201-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="ae201-180">**Tuotteen laatu** -skenaarion määrittäminen Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="ae201-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="ae201-181">**Tuotteen laatu** -skenaario luo ilmoituksen, jos nimikkeen määrite on määritetyn alueen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="ae201-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="ae201-182">Anturi voi esimerkiksi lähettää kunkin nimikkeen painon IoT-keskittimeen.</span><span class="sxs-lookup"><span data-stu-id="ae201-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="ae201-183">Ilmoitus luodaan Supply Chain Managementissa, jos nimike oli liian raskas tai liian kevyt.</span><span class="sxs-lookup"><span data-stu-id="ae201-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="ae201-184">Skenaariossa on seuraavat riippuvuudet:</span><span class="sxs-lookup"><span data-stu-id="ae201-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="ae201-185">Tuotantotilauksen on oltava käynnissä yhdistetyssä koneessa ja valmistamassa tuotetta, jossa on yhdistetty erämäärite, jotta hälytys käynnistyy.</span><span class="sxs-lookup"><span data-stu-id="ae201-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="ae201-186">IoT-keskittimeen lähetettävässä erämääritteen ilmaisevalla signaalilla on oltava yksilöivä ominaisuuden nimi.</span><span class="sxs-lookup"><span data-stu-id="ae201-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="ae201-187">IoT-keskittimen sanomassa on oltava Unix-millisekunnin aikaleimaominaisuus.</span><span class="sxs-lookup"><span data-stu-id="ae201-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="ae201-188">**Tuotannon viivästykset** -skenaarion määrittäminen Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="ae201-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="ae201-189">**Tuotannon viivästykset** -skenaario luo ilmoituksen, jos tuotantokapasiteetti alittaa raja-arvon.</span><span class="sxs-lookup"><span data-stu-id="ae201-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="ae201-190">Tässä skenaariossa kunkin tuotetun nimikkeen **PartOut**-signaali lähetetään IoT-keskittimeen.</span><span class="sxs-lookup"><span data-stu-id="ae201-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="ae201-191">Tilauksen viivästyminen lasketaan Supply Chain Managementissa sen perusteella, kuinka pitkäksi tuotantotilauksen suorittaminen ajoitettu, kuinka monta nimikettä tuotetaan, kuinka kauan työ on ollut meneillään ja kuinka monta **PartOut**-signaalia vastaanotetaan.</span><span class="sxs-lookup"><span data-stu-id="ae201-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="ae201-192">Viivästysilmoitus luodaan, jos työn **PartOut**-signaalien määrä alittaa odotetun arvon raja-arvon.</span><span class="sxs-lookup"><span data-stu-id="ae201-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="ae201-193">Skenaariossa on seuraavat riippuvuudet:</span><span class="sxs-lookup"><span data-stu-id="ae201-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="ae201-194">Tuotantotilauksen on oltava meneillään yhdistetyssä koneessa, jotta hälytys käynnistyy.</span><span class="sxs-lookup"><span data-stu-id="ae201-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="ae201-195">IoT-keskittimeen lähetettävässä yhdistetyn koneen Osa pois käytöstä -signaalilla on oltava yksilöivä ominaisuuden nimi.</span><span class="sxs-lookup"><span data-stu-id="ae201-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="ae201-196">IoT-keskittimen sanomassa on oltava Unix-millisekunnin aikaleimaominaisuus.</span><span class="sxs-lookup"><span data-stu-id="ae201-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="ae201-197">Skenaarion poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="ae201-197">How to disable a scenario</span></span>

<span data-ttu-id="ae201-198">Skenaario poistetaan käytöstä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ae201-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="ae201-199">Valitse Supply Chain Managementissa **Tuotannonhallinta \> Asetukset \> IoT-analytiikka \> Skenaarionhallinta**.</span><span class="sxs-lookup"><span data-stu-id="ae201-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="ae201-200">Valitse skenaariossa **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="ae201-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="ae201-201">Siirry ohjatun toiminnon viimeiseen välilehteen valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="ae201-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="ae201-202">Poista skenaario käytöstä siirtämällä liukusäädintä.</span><span class="sxs-lookup"><span data-stu-id="ae201-202">Toggle the slider to disable the scenario.</span></span>
