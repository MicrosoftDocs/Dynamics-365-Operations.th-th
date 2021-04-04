---
title: ซิงโครไนส์วันที่และเวลาในงานการนําเข้า
description: ใช้โซนเวลา UTC ในงานการนําเข้าเพื่อหลีกเลี่ยงปัญหากับการแปลงโซนเวลา
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ce3bf39e8342d3fe19a253f6d17684b2bd0aec0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570492"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="47f40-103">ซิงโครไนส์วันที่และเวลาในงานการนําเข้า</span><span class="sxs-lookup"><span data-stu-id="47f40-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47f40-104">เป็นสิ่งสำคัญที่ต้องตั้งค่าโซนเวลาให้กับงานการนําเข้าของคุณเป็น Coordinated Universal Time (UTC)</span><span class="sxs-lookup"><span data-stu-id="47f40-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="47f40-105">คุณอาจเห็นวันที่และเวลาที่ไม่คาดคิดในข้อมูลที่นําเข้าของคุณ ถ้าคุณใช้การตั้งค่าอื่น</span><span class="sxs-lookup"><span data-stu-id="47f40-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="47f40-106">โดยไม่มีการตั้งค่าที่ถูกต้อง กระบวนการนําเข้าจะแปลงวันที่ UTC เป็นรูปแบบเฉพาะที่ และจากนั้น การตั้งค่าระบบจะแปลงค่านั้นอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="47f40-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="47f40-107">การแปลงแบบคู่นี้ส่งผลให้เกิดการเปลี่ยนแปลงวันที่ระหว่างแอปพลิเคชันต่างๆ</span><span class="sxs-lookup"><span data-stu-id="47f40-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="47f40-108">ตัวอย่างเช่น การแปลงแบบคู่อาจทําให้วันที่เริ่มต้นของพนักงานแตกต่างกันระหว่างกัน Dynamics 365 Human Resources และ Dynamics 365 Finance เนื่องจากความแตกต่างในโซนเวลาเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="47f40-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="47f40-109">การตั้งค่างานการนําเข้าเป็น UTC จะแก้ไขปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="47f40-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="47f40-110">ใน Dynamics 365 Finance and Operations ให้เลือก **การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="47f40-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="47f40-111">เลือก **นําเข้าโครงการ** แล้วจากนั้น เลือกโครงการ</span><span class="sxs-lookup"><span data-stu-id="47f40-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="47f40-112">ภายใต้ **รูปแบบวันที่ต้นทาง** ให้เลือก **CSV-Unicode**</span><span class="sxs-lookup"><span data-stu-id="47f40-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="47f40-113">[![เปลี่ยนรูปแบบวันที่ต้นทางเป็น UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="47f40-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="47f40-114">เปลี่ยน **โซนเวลา** เป็น **Coordinated Universal Timezone** และเปลี่ยน **ภาษา** เป็น **En-US**</span><span class="sxs-lookup"><span data-stu-id="47f40-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]