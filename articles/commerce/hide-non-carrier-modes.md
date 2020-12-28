---
title: ซ่อนวิธีการจัดส่งที่ไม่ใช่ผู้ขนส่งจากตัวเลือกการจัดส่งใน POS
description: หัวข้อนี้จะอธิบายถึงตัวเลือกการกำหนดค่าที่สามารถป้องกันไม่ให้มีแสดงการจัดส่งสินค้าที่ไม่ใช่ผู้ขนส่งให้ปรากฏสำหรับการเลือก เมื่อมีการสร้างใบสั่งการจัดส่งในแอพลิเคชันขายหน้าร้าน (POS)
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 38d57ed5f8d2b8725cd11156f0135988bb76e047
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416216"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="0ba6a-103">ซ่อนวิธีการจัดส่งที่ไม่ใช่ผู้ขนส่งจากตัวเลือกการจัดส่งใน POS</span><span class="sxs-lookup"><span data-stu-id="0ba6a-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0ba6a-104">หัวข้อนี้อธิบายถึงตัวเลือกการกำหนดค่าที่พร้อมใช้งานสำหรับแอพลิเคชันขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="0ba6a-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="0ba6a-105">ตัวเลือกการกำหนดค่านี้จะเปลี่ยนลักษณะการทำงานสำหรับการเลือกวิธีการจัดส่งเมื่อสร้างใบสั่งการจัดส่งใน POS</span><span class="sxs-lookup"><span data-stu-id="0ba6a-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="0ba6a-106">เมื่อผู้ใช้สร้างใบสั่งการจัดส่งสินค้าของลูกค้าใน POS ผู้ใช้จะสามารถเลือกวิธีการจัดส่งสำหรับการจัดส่งสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="0ba6a-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="0ba6a-107">ฟังก์ชันนี้จะพร้อมใช้งานโดยไม่คำนึงว่าจะมีการจัดส่งสินค้าตามใบสั่งทั้งหมดหรือเฉพาะรายการที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ba6a-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="0ba6a-108">ตามค่าเริ่มต้น กล่องโต้ตอบที่มีการเลือกวิธีการจัดส่งจะแสดงวิธีการจัดส่งที่ใช้ได้ทั้งหมดสำหรับชุดของช่องทาง สินค้าและที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0ba6a-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="0ba6a-109">วิธีการจัดส่งเหล่านี้มีการกำหนดไว้บนหน้า **วิธีการจัดส่ง** ในศูนย์ควบคุม (**การขายและการตลาด \> การตั้งค่า \> การกระจายสินค้า \>  วิธีการจัดส่ง**)</span><span class="sxs-lookup"><span data-stu-id="0ba6a-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="0ba6a-110">วิธีการจัดส่งที่ไม่ใช่ผู้ขนส่ง เช่น **ยกของ** หรือ **รถบรรทุก** อาจปรากฏขึ้นให้เลือกในกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="0ba6a-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="0ba6a-111">อย่างไร ก็ตามมีคุณลักษณะที่ช่วยให้คุณสามารถซ่อนวิธีการจัดส่งที่ไม่ใช่ผู้ขนส่งในกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="0ba6a-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="0ba6a-112">ในการเปิดคุณลักษณะนี้ บนหน้า **พารามิเตอร์ Commerce** บนแท็บ **ใบสั่งของลูกค้า** ให้ตั้งค่าตัวเลือก **แสดงเฉพาะตัวเลือกวิธีการจัดส่งที่ใช้ผู้ขนส่งสำหรับการส่งสินค้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0ba6a-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="0ba6a-113">หลังจากที่คุณเปิดใช้งานคุณลักษณะนี้และเรียกใช้งานการกระจายสินค้าที่เหมาะสมเพื่อซิงค์ข้อมูลไปยังฐานข้อมูลช่องทาง วิธีการจัดส่งที่ไม่ใช่ผู้ขนส่งจะไม่ปรากฏให้เลือกในระหว่างกระบวนการสร้างใบสั่งจัดส่งใน POS</span><span class="sxs-lookup"><span data-stu-id="0ba6a-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>
