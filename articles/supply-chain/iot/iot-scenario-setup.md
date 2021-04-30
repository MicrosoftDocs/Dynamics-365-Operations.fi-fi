---
title: IoT-analytiikkaskenaarion määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten IoT-analytiikan skenaarioita voidaan määrittää Microsoft Dynamics 365 Supply Chain Managementissa.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 36be4a85dbbd28839afd45b6ed167b4c8181ae72
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909498"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="8073a-103">IoT-analytiikkaskenaarion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8073a-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8073a-104">Tässä ohjeaiheessa kerrotaan, miten IoT-analytiikan skenaarioita voidaan määrittää Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="8073a-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8073a-105">Ennen kuin voit määrittää skenaarioita, sinun on [Määritettävä Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="8073a-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="8073a-106">Tässä ohjeaiheessa määritetään **Laiteseisokki**-skenaario siten, että Supply Chain Managementissa luodaan ilmoitus, kun kone sammuu.</span><span class="sxs-lookup"><span data-stu-id="8073a-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="8073a-107">Tässä kerrotaan myös, miten **Tuotteen laatu** -skenaario määritetään siten, että järjestelmä luo ilmoituksen, jos nimikkeen määrite on määritetyn alueen ulkopuolella, ja miten **Tuotantoviiveet**-skenaario määritetään siten, että järjestelmä luo ilmoituksen, jos tuotantomäärä alittaa raja-arvon.</span><span class="sxs-lookup"><span data-stu-id="8073a-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="8073a-108">Laiteseisokki-skenaarion määrittäminen Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="8073a-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="8073a-109">**Laiteseisokki**-skenaariossa **PartOut**-signaali yhdistetään koneen hälytysrajaan.</span><span class="sxs-lookup"><span data-stu-id="8073a-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="8073a-110">Konetta valvotaan vain silloin, kun se on valittu skenaarioon ja määritetty **Käynnissä**-tilaan Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="8073a-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="8073a-111">Jos koneen viimeisestä koneelta vastaanotetusta **PartOut** -signaalista kulunut aika on suurempi kuin hälytysraja, **Kone sammunut** -ilmoitus käynnistetään.</span><span class="sxs-lookup"><span data-stu-id="8073a-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="8073a-112">Jos kone on edelleen käynnissä, **Kone käynnissä** -ilmoitus luodaan, kun seuraava **PartOut**-signaali vastaanotetaan.</span><span class="sxs-lookup"><span data-stu-id="8073a-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="8073a-113">Jos kone pysyy sammuneena 30 minuuttia, luodaan uusi **Kone sammunut** -ilmoitus.</span><span class="sxs-lookup"><span data-stu-id="8073a-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="8073a-114">**Laiteseisokki**-skenaariossa on seuraavat riippuvuudet:</span><span class="sxs-lookup"><span data-stu-id="8073a-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="8073a-115">Hälytys luodaan vain, jos tuotantotilaus on meneillään yhdistetyssä koneessa.</span><span class="sxs-lookup"><span data-stu-id="8073a-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="8073a-116">Yhdistetyn koneen **PartOut**-signaalia vastaava signaali on lähetettävä IoT-keskittimeen, ja signaalilla on oltava yksilöivä ominaisuuden nimi.</span><span class="sxs-lookup"><span data-stu-id="8073a-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="8073a-117">Azuren IoT-keskittemen sanomassa on oltava UNIX-**aikaleima**-ominaisuus, jossa arvo ilmaistaan millisekunteina (ms).</span><span class="sxs-lookup"><span data-stu-id="8073a-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="8073a-118">Skenaario määritetään seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8073a-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="8073a-119">Kirjaudu Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="8073a-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="8073a-120">Ota IoT-analytiikkatoiminnon merkintä käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8073a-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="8073a-121">Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8073a-121">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="8073a-122">Määritä mittarit.</span><span class="sxs-lookup"><span data-stu-id="8073a-122">Configure the metrics.</span></span> <span data-ttu-id="8073a-123">Lisätietoja on kohdassa [Mittarien määrittäminen](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="8073a-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="8073a-124">Siirry kohtaan **Tuotannonhallinta \> Määritys \> IoT-analytiikka \> Skenaarionhallinta**.</span><span class="sxs-lookup"><span data-stu-id="8073a-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="8073a-125">Valitse **Laiteseisokki**-ruudussa **Määritä** avataksesi ohjatun määritystoiminnon.</span><span class="sxs-lookup"><span data-stu-id="8073a-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="8073a-126">Ohjatun määritystoiminnon ensimmäinen sivu on **Laiteanturin rakennemääritys**.</span><span class="sxs-lookup"><span data-stu-id="8073a-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="8073a-127">Tällä sivulla sinun tavoitteenasi on määrittää rakenne Supply Chain Managementissa siten, että se vastaa IoT-keskittimen sanomien JavaScript Object Notation (JSON) -muotoa.</span><span class="sxs-lookup"><span data-stu-id="8073a-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="8073a-128">Sanomarakenteita voi määrittää useita.</span><span class="sxs-lookup"><span data-stu-id="8073a-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="8073a-129">Lisätietoja on kohdassa [Rakennemuodot IoT-keskitinsanomille](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="8073a-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="8073a-130">Tässä esimerkissä sanoma sisältää seuraavan muotoisen sanomaerän:</span><span class="sxs-lookup"><span data-stu-id="8073a-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

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

7. <span data-ttu-id="8073a-131">Lisää rivi taulukkoon ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="8073a-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="8073a-132">Määritä **Rakenteen nimi** -kentän arvoksi **ID**.</span><span class="sxs-lookup"><span data-stu-id="8073a-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="8073a-133">Määritä **Rakenteen polku** -kentän arvoksi **/payload\[\*\]/id**.</span><span class="sxs-lookup"><span data-stu-id="8073a-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="8073a-134">Määritä **Kuvaus**-kentän arvoksi **Sanoman tunnus**.</span><span class="sxs-lookup"><span data-stu-id="8073a-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="8073a-135">Lisää uusi rivi taulukkoon ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="8073a-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="8073a-136">Määritä **Rakenteen nimi** -kentän arvoksi **Timestamp**.</span><span class="sxs-lookup"><span data-stu-id="8073a-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="8073a-137">Määritä **Rakenteen polku** -kentän arvoksi **/payload\[\*\]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="8073a-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="8073a-138">Määritä **Kuvaus**-kentän arvoksi **Sanoman aikaleima**.</span><span class="sxs-lookup"><span data-stu-id="8073a-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="8073a-139">Lisää uusi rivi taulukkoon ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="8073a-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="8073a-140">Määritä **Rakenteen nimi** -kentän arvoksi **Arvo**.</span><span class="sxs-lookup"><span data-stu-id="8073a-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="8073a-141">Määritä **Rakenteen polku** -kentän arvoksi **/payload\[\*\]/arvo**.</span><span class="sxs-lookup"><span data-stu-id="8073a-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="8073a-142">Määritä **Kuvaus**-kentän arvoksi **Sanoman arvo**.</span><span class="sxs-lookup"><span data-stu-id="8073a-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8073a-143">Kaikkia sanoman ominaisuuksia ei tarvitse määrittää.</span><span class="sxs-lookup"><span data-stu-id="8073a-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="8073a-144">Määritä vain ominaisuudet, joita tarvitset.</span><span class="sxs-lookup"><span data-stu-id="8073a-144">Define only the properties that you require.</span></span> <span data-ttu-id="8073a-145">Edellisissä vaiheissa et luonut riviä **Juuren aikaleima**.</span><span class="sxs-lookup"><span data-stu-id="8073a-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="8073a-146">**Juuren aikaleima** -polku olisi **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="8073a-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="8073a-147">Siirry **Laiteanturin rakenteen yhdistämismääritys** -sivulle valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="8073a-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="8073a-148">Määritä **Laitteen resurssitunnus** -rivin **Rakenteen nimi** -kentän arvoksi **ID**.</span><span class="sxs-lookup"><span data-stu-id="8073a-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="8073a-149">Määritä **UTC-aika**-rivin **Rakenteen rivi** -kentän arvoksi **Timestamp**.</span><span class="sxs-lookup"><span data-stu-id="8073a-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="8073a-150">Määritä **Osan tuottama signaali** -rivin **Rakenteen nimi** -kentän arvoksi **Arvo**.</span><span class="sxs-lookup"><span data-stu-id="8073a-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="8073a-151">Siirry **Laitteen resurssitunnuksen määritys** -sivulle valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="8073a-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="8073a-152">Näiden ohjeiden avulla IoT-keskittimen sanoman arvot yhdistetään Supply Chain Managementin resursseihin:</span><span class="sxs-lookup"><span data-stu-id="8073a-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="8073a-153">Lisää uusi rivi **Signaalitietoarvot**-taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="8073a-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="8073a-154">Syötä **Arvo**-kenttään **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="8073a-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="8073a-155">Tämä arvo saadaan IoT-keskittimen sanoman JSON **id** -ominaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="8073a-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="8073a-156">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8073a-156">Select **Save**.</span></span>
    3. <span data-ttu-id="8073a-157">Valitse **Liiketoimintatietueen yhdistäminen** -taulussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8073a-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="8073a-158">Kentälle **Liiketoimintatietueen tyyppi** täytetään automaattisesti oletusarvo, eikä sitä tarvitse muuttaa.</span><span class="sxs-lookup"><span data-stu-id="8073a-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="8073a-159">Valitse **Liiketoimintatietue**-kentässä, se Supply Chain Managementin koneresurssi, josta signaalin arvo lähetetään.</span><span class="sxs-lookup"><span data-stu-id="8073a-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="8073a-160">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8073a-160">Select **Save**.</span></span>
    6. <span data-ttu-id="8073a-161">Lisää koneen **Machine1226** uusi tietueen yhdistämismääritys toistamalla nämä vaiheet.</span><span class="sxs-lookup"><span data-stu-id="8073a-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="8073a-162">Useita signaalin tietoarvoja voi yhdistää yhteen Supply Chain Managementin tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="8073a-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="8073a-163">Valitse käsiteltävät koneet **Valitut**-sarakkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="8073a-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="8073a-164">Kaikkia signaalin arvoja ei tarvitse määrittää eikä kaikkia koneita tarvitse valita.</span><span class="sxs-lookup"><span data-stu-id="8073a-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="8073a-165">Siirry **Osan tuottaman signaalin määritys** -sivulle valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="8073a-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="8073a-166">Lisää **Signaalin tietoarvot** -taulussa uusi rivi, ja määritä **Arvo**-kentän arvoksi **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="8073a-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="8073a-167">Tämä arvo saadaan IoT-keskittimen sanoman JSON **value** -ominaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="8073a-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="8073a-168">Voit lisätä skenaarioon tarvittavan määrän arvoja.</span><span class="sxs-lookup"><span data-stu-id="8073a-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="8073a-169">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8073a-169">Select **Save**.</span></span>
20. <span data-ttu-id="8073a-170">Siirry **Laiteseisokin raja-arvo** -sivulle valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="8073a-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="8073a-171">Luettelossa olevat koneet on yhdistetty aiemmin signaalin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="8073a-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="8073a-172">Tällä sivulla määritetään raja-arvo määrittämään, onko kone sammunut.</span><span class="sxs-lookup"><span data-stu-id="8073a-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="8073a-173">Jos raja-arvoksi määritetään esimerkiksi **10**, Supply Chain Management luo ilmoituksen, jos koneelta ei saada **PartOut** -signaalia 10 minuuttiin.</span><span class="sxs-lookup"><span data-stu-id="8073a-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="8073a-174">Siirry **Ota skenaario käyttöön** -sivulle valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="8073a-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="8073a-175">Ota skenaario käyttöön määrittämällä asetus.</span><span class="sxs-lookup"><span data-stu-id="8073a-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="8073a-176">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="8073a-176">Select **Finish**.</span></span>

<span data-ttu-id="8073a-177">Skenaarion määritys on nyt valmis.</span><span class="sxs-lookup"><span data-stu-id="8073a-177">The scenario setup is now completed.</span></span> <span data-ttu-id="8073a-178">IoT-analytiikka aloittaa automaattisesti IoT-keskittimen sanomien käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="8073a-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="8073a-179">Tuotteen laatu -skenaarion määrittäminen Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="8073a-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="8073a-180">**Tuotteen laatu** -skenaario luo ilmoituksen, jos nimikkeen määrite on määritetyn alueen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="8073a-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="8073a-181">Anturi voi esimerkiksi lähettää kunkin nimikkeen painon IoT-keskittimeen.</span><span class="sxs-lookup"><span data-stu-id="8073a-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="8073a-182">Jos jokin nimike on liian painava tai kevyt Supply Chain Managementissa luodaan ilmoitus.</span><span class="sxs-lookup"><span data-stu-id="8073a-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="8073a-183">**Tuotteen laatu** -skenaariossa on seuraavat riippuvuudet:</span><span class="sxs-lookup"><span data-stu-id="8073a-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="8073a-184">Hälytys voi käynnistyä vain, jos tuotantotilaus on käynnissä yhdistetyssä koneessa ja valmistamassa tuotetta, jossa on yhdistetty erämäärite.</span><span class="sxs-lookup"><span data-stu-id="8073a-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="8073a-185">IoT-keskittimeen lähetettävässä erämääritteen ilmaisevalla signaalilla on oltava yksilöivä ominaisuuden nimi.</span><span class="sxs-lookup"><span data-stu-id="8073a-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="8073a-186">IoT-keskittemen sanomassa on oltava UNIX-**aikaleima**-ominaisuus, jossa arvo ilmaistaan millisekunteina (ms).</span><span class="sxs-lookup"><span data-stu-id="8073a-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="8073a-187">Tuotannon viivästykset -skenaarion määrittäminen Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="8073a-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="8073a-188">**Tuotannon viivästykset** -skenaario luo ilmoituksen, jos tuotantokapasiteetti alittaa raja-arvon.</span><span class="sxs-lookup"><span data-stu-id="8073a-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="8073a-189">Tässä skenaariossa kunkin tuotetun nimikkeen **PartOut**-signaali lähetetään IoT-keskittimeen.</span><span class="sxs-lookup"><span data-stu-id="8073a-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="8073a-190">Supply Chain Managementissa tilausviive lasketaan sen ajan perusteella, joka tuotantotilausta on tarkoitus suorittaa, tuotettavien nimikkeiden määrän perusteella, tehtävän käynnissäoloajan perusteella sekä vastaanotettujen **PartOut**-signaalien perusteella.</span><span class="sxs-lookup"><span data-stu-id="8073a-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="8073a-191">Viivästysilmoitus luodaan, jos työn **PartOut**-signaalien määrä alittaa raja-arvon.</span><span class="sxs-lookup"><span data-stu-id="8073a-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="8073a-192">**Tuotantoviiveet** -skenaariossa on seuraavat riippuvuudet:</span><span class="sxs-lookup"><span data-stu-id="8073a-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="8073a-193">Hälytys luodaan vain, jos tuotantotilaus on meneillään yhdistetyssä koneessa.</span><span class="sxs-lookup"><span data-stu-id="8073a-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="8073a-194">Yhdistetyn koneen **PartOut**-signaalia vastaava signaali on lähetettävä Azuren IoT-keskittimeen, ja signaalilla on oltava yksilöivä ominaisuuden nimi.</span><span class="sxs-lookup"><span data-stu-id="8073a-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="8073a-195">IoT-keskittemen sanomassa on oltava UNIX-**aikaleima**-ominaisuus, jossa arvo ilmaistaan millisekunteina (ms).</span><span class="sxs-lookup"><span data-stu-id="8073a-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="8073a-196">Skenaarion poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="8073a-196">Disable a scenario</span></span>

<span data-ttu-id="8073a-197">Skenaario poistetaan käytöstä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8073a-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="8073a-198">Siirry Supply Chain Managementissa kohtaan **Tuotannonhallinta \> Asetukset \> IoT-analytiikka \> Skenaarionhallinta**.</span><span class="sxs-lookup"><span data-stu-id="8073a-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="8073a-199">Valitse skenaarion ruudussa **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="8073a-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="8073a-200">Siirry ohjatun toiminnon viimeiselle sivulle valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="8073a-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="8073a-201">Poista skenaario käytöstä määrittämällä asetus.</span><span class="sxs-lookup"><span data-stu-id="8073a-201">Set the option to disable the scenario.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]