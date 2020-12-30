---
title: ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และ Dataverse
description: หัวข้อนี้จะอธิบายถึงวิธีการที่คุณสามารถกำหนดได้ว่า มีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และใน Dataverse หรือไม่
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f389bcf133cc7e6a086167d5e26c1b8795d0fa30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685550"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="24cc8-103">ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="24cc8-103">Verify that dual-write is configured in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="24cc8-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="24cc8-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="24cc8-105">กล่าวคือ จะอธิบายถึงวิธีการที่คุณสามารถกำหนดได้ว่า มีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และใน Dataverse หรือไม่</span><span class="sxs-lookup"><span data-stu-id="24cc8-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="24cc8-106">ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="24cc8-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="24cc8-107">เมื่อต้องการตรวจสอบว่า ข้อผิดพลาดที่คุณเห็นเมื่อคุณพยายามบันทึกแถวสำหรับการปรับปรุงมาจากการรวมแบบสองทิศทางหรือไม่ ก่อนอื่นให้ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="24cc8-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="24cc8-108">ถ้าคุณมีสิทธิ์ระดับผู้ดูแลระบบในแอป Finance and Operations ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือกไทล์ **การรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="24cc8-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="24cc8-109">ถ้ารายละเอียดของสภาพแวดล้อมที่มีการเชื่อมโยงและรายการของแผนผังตารางที่กำลังรันถูกแสดง จะมีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="24cc8-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![การตรวจสอบความถูกต้องของการเชื่อมต่อแอป Finance and Operations เมื่อคุณมีสิทธิ์ระดับผู้ดูแลระบบ](media/verify_fin_ops_1.png)

+ <span data-ttu-id="24cc8-111">ถ้าคุณไม่มีสิทธิ์ของผู้ดูแลระบบ คุณจะได้รับข้อความแสดงข้อผิดพลาด *ไม่สามารถเขียนข้อมูลไปยังเอนทิตีได้ \<entity name\>*</span><span class="sxs-lookup"><span data-stu-id="24cc8-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="24cc8-112">ในตัวอย่างในภาพประกอบต่อไปนี้ คุณไม่สามารถสร้างแถวลูกค้าในแอป Finance and Operations ได้ เนื่องจากมีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง แต่กลุ่มลูกค้าและข้อมูลอ้างอิงเงื่อนไขการชำระเงินไม่มีอยู่ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="24cc8-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![การตรวจสอบความถูกต้องของการเชื่อมต่อแอป Finance and Operations เมื่อคุณไม่มีสิทธิ์ระดับผู้ดูแลระบบ](media/verify_fin_ops_2.png)

<span data-ttu-id="24cc8-114">สำหรับข้อมูลเกี่ยวกับวิธีการแก้ไขปัญหา เมื่อคุณสร้างข้อมูลในแอป Finance and Operations ให้ดูที่ [แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง](dual-write-troubleshooting-live-sync.md)</span><span class="sxs-lookup"><span data-stu-id="24cc8-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="24cc8-115">ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="24cc8-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="24cc8-116">เมื่อคุณสร้างข้อมูล ถ้าคุณเห็นฟิลด์ **บริษัท** บนหน้าใน Dataverse จะมีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="24cc8-116">When you create data, if you see the **Company** field on pages in Dataverse, dual-write is configured.</span></span>

![การตรวจสอบการเชื่อมต่อ Dataverse](media/verify_cds.png)

<span data-ttu-id="24cc8-118">สำหรับข้อมูลเกี่ยวกับวิธีการแก้ไขปัญหา เมื่อคุณสร้างข้อมูลใน Dataverse ให้ดูที่ [แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง](dual-write-troubleshooting-live-sync.md)</span><span class="sxs-lookup"><span data-stu-id="24cc8-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="24cc8-119">สำหรับข้อมูลเกี่ยวกับวิธีการดูรายละเอียดข้อผิดพลาด ถ้าคุณพบข้อผิดพลาดใดๆ ในขณะที่คุณสร้างข้อมูลใน Dataverse ให้ดูที่ให้ดูที่ [เปิดใช้งานและดูล็อกการติดตามปลั๊กอินใน Dataverse เพื่อดูรายละเอียดข้อผิดพลาด](dual-write-troubleshooting.md#enable-view-trace)</span><span class="sxs-lookup"><span data-stu-id="24cc8-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>
