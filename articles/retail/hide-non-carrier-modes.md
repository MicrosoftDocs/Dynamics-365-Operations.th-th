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
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 09ea83b3336b208f8af0a91025c2e6c50d64c385
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/24/2019
ms.locfileid: "2659032"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="cb725-103">ซ่อนวิธีการจัดส่งที่ไม่ใช่ผู้ขนส่งจากตัวเลือกการจัดส่งใน POS</span><span class="sxs-lookup"><span data-stu-id="cb725-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cb725-104">หัวข้อนี้อธิบายถึงตัวเลือกการกำหนดค่าที่พร้อมใช้งานสำหรับแอพลิเคชันขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="cb725-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="cb725-105">ตัวเลือกการกำหนดค่านี้จะเปลี่ยนลักษณะการทำงานสำหรับการเลือกวิธีการจัดส่งเมื่อสร้างใบสั่งการจัดส่งใน POS</span><span class="sxs-lookup"><span data-stu-id="cb725-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="cb725-106">เมื่อผู้ใช้สร้างใบสั่งการจัดส่งสินค้าของลูกค้าใน POS ผู้ใช้จะสามารถเลือกวิธีการจัดส่งสำหรับการจัดส่งสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="cb725-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="cb725-107">ฟังก์ชันนี้จะพร้อมใช้งานโดยไม่คำนึงว่าจะมีการจัดส่งสินค้าตามใบสั่งทั้งหมดหรือเฉพาะรายการที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cb725-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="cb725-108">ตามค่าเริ่มต้น กล่องโต้ตอบที่มีการเลือกวิธีการจัดส่งจะแสดงวิธีการจัดส่งที่ใช้ได้ทั้งหมดสำหรับชุดของช่องทาง สินค้าและที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="cb725-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="cb725-109">วิธีการจัดส่งเหล่านี้มีการกำหนดไว้บนเพจ **วิธีการจัดส่ง** ใน Retail Headquarters (**การขายและการตลาด \> การตั้งค่า \> การกระจายสินค้า \> วิธีการจัดส่ง**)</span><span class="sxs-lookup"><span data-stu-id="cb725-109">These modes of delivery are defined on the **Modes of delivery** page in Retail Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="cb725-110">วิธีการจัดส่งที่ไม่ใช่ผู้ขนส่ง เช่น **ยกของ** หรือ **รถบรรทุก** อาจปรากฏขึ้นให้เลือกในกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="cb725-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="cb725-111">อย่างไร ก็ตามมีคุณลักษณะที่ช่วยให้คุณสามารถซ่อนวิธีการจัดส่งที่ไม่ใช่ผู้ขนส่งในกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="cb725-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="cb725-112">ในการเปิดคุณลักษณะนี้ บนเพจ **พารามิเตอร์การขายปลีก** บนแท็บ **ใบสั่งของลูกค้า** ให้ตั้งค่าตัวเลือก **แสดงเฉพาะวิธีการจัดส่งที่ใช้ผู้ขนส่งสำหรับการส่งสินค้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cb725-112">To turn on this feature, on the **Retail parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="cb725-113">หลังจากที่คุณเปิดใช้งานคุณลักษณะนี้และเรียกใช้งานการกระจายสินค้าที่เหมาะสมเพื่อซิงค์ข้อมูลไปยังฐานข้อมูลช่องทาง วิธีการจัดส่งที่ไม่ใช่ผู้ขนส่งจะไม่ปรากฏให้เลือกในระหว่างกระบวนการสร้างใบสั่งจัดส่งใน POS</span><span class="sxs-lookup"><span data-stu-id="cb725-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>
