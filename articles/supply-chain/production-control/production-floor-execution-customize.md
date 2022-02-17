---
title: กำหนดอินเทอร์เฟสการดำเนินการผลิต
description: หัวข้อนี้อธิบายวิธีการขยายแบบฟอร์มปัจจุบัน หรือสร้างแบบฟอร์มและปุ่มใหม่ให้กับอินเทอร์เฟสการปฏิบัติการในการผลิต
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 67fb381cbef6f1673afcaa834666b4a859bdf4e6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066557"
---
# <a name="customize-the-production-floor-execution-interface"></a>กำหนดอินเทอร์เฟสการดำเนินการผลิต

[!include [banner](../includes/banner.md)]

นักพัฒนาสามารถขยายแบบฟอร์มปัจจุบัน หรือสร้างแบบฟอร์มและปุ่มของพวกเขาเองให้กับอินเทอร์เฟสการปฏิบัติการในการผลิต หลังจากที่คุณได้เพิ่มรหัสให้กับองค์ประกอบใหม่เหล่านี้ ผู้ดูแลระบบ หรือผู้จัดการการผลิตจะสามารถเพิ่มรหัสดังกล่าวในอินเทอร์เฟสได้อย่างง่ายดาย โดยการใช้ตัวควบคุมการตั้งค่าคอนฟิกมาตรฐาน

ตัวอย่างเช่น ต่อไปนี้เป็นโซลูชันที่เป็นไปได้บางอย่าง ถ้าต้องใช้คอลัมน์ใหม่ในแบบฟอร์มหลัก

- ขยายแบบฟอร์ม `JmgProductionFloorExecutionMainGrid` และเพิ่มฟิลด์ที่ต้องการ
- สร้างแบบฟอร์มใหม่ และเพิ่มเป็นมุมมองหลักใหม่ (แท็บ)

## <a name="add-a-new-button-action"></a>เพิ่มปุ่มใหม่ (การดำเนินการ)

ในการเพิ่มปุ่มใหม่ (การดําเนินการ) ให้ปฏิบัติตามขั้นตอนเหล่านี้ เพื่อสร้างคลาสที่ใช้การดําเนินการที่กำหนดเองของคุณ

1. สร้างคลาสใหม่ที่มีชื่อว่า `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action` โดยที่:

    - `<ExtensionPrefix>` ระบุโซลูชันของคุณ โดยทั่วไปใช้ชื่อบริษัทของคุณ
    - `<ActionName>` เป้นชื่อเฉพาะสำหรับคลาส ซึ่งโดยทั่วไปจะระบุชนิดของการดำเนินการ

1. คลาสใหม่ต้องขยายคลาส `JmgProductionFloorExecutionAction`
1. แทนที่วิธีการที่จําเป็นทั้งหมด

ตัวอย่างเช่น ให้ดูโค้ดของคลาสต่อไปนี้:

- `JmgProductionFloorExecutionBreakAction` – คลาสสำหรับการดำเนินการอย่างง่าย ที่ไม่ต้องใช้เรกคอร์ดใดๆ
- `JmgProductionFloorExecutionReportFeedbackAction` – คลาสที่ให้ฟังก์ชันที่ซับซ้อนมากขึ้น

เมื่อคุณเสร็จสิ้นแล้ว ปุ่มใหม่ (การดำเนินการ) จะแสดงรายการบนหน้า **แท็บการออกแบบ** ใน Microsoft Dynamics 365 Supply Chain Management โดยอัตโนมัติ คุณ (หรือผู้ดูแลระบบ หรือผู้จัดการฝ่ายผลิต) สามารถเพิ่มไปยังแถบเครื่องมือหลักหรือรองได้อย่างง่ายดาย เช่นเดียวกับที่คุณสามารถเพิ่มปุ่มมาตรฐานได้ สำหรับคำแนะนำ ให้ดูที่ [ออกแบบอินเทอร์เฟสการดำเนินการผลิต](production-floor-execution-tabs.md)

## <a name="add-a-new-main-view"></a>เพิ่มมุมมองหลักใหม่

1. สร้างแบบฟอร์มใหม่ที่มีองค์ประกอบและฟังก์ชันที่ต้องการ โปรดทราบว่าแบบฟอร์มนี้เป็นแบบฟอร์มใหม่ ไม่ใช่ส่วนขยาย ตั้งชื่อแบบฟอร์ม `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>` โดยที่:

    - `<ExtensionPrefix>` ระบุโซลูชันของคุณ โดยทั่วไปใช้ชื่อบริษัทของคุณ
    - `<FormName>` เป้นชื่อเฉพาะสำหรับแบบฟอร์ม

1. สร้างรายการเมนูที่ชื่อ `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`
1. สร้างส่วนขยายที่ชื่อ `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` โดยที่วิธีการ `getMainMenuItemsList` จะถูกขยายโดยเพิ่มรายการเมนูใหม่ลงในรายการ รหัสต่อไปนี้แสดงตัวอย่าง

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

เมื่อคุณเสร็จสิ้นแล้ว มุมมองหลักใหม่จะแสดงรายการโดยอัตโนมัติในกล่องชุดคอมโบ **มุมมองหลัก** ในหน้า **แท็บการออกแบบ** ใน Supply Chain Management คุณ (หรือผู้ดูแลระบบ หรือผู้จัดการฝ่ายผลิต) สามารถเพิ่มไปยังแท็บใหม่หรือแท็บที่มีอยู่แล้วได้อย่างง่ายดาย เช่นเดียวกับที่คุณสามารถเพิ่มมุมมองหลักมาตรฐานได้ สำหรับคำแนะนำ ให้ดูที่ [ออกแบบอินเทอร์เฟสการดำเนินการผลิต](production-floor-execution-tabs.md)

## <a name="add-a-details-view"></a>เพิ่มมุมมองรายละเอียด

1. สร้างแบบฟอร์มใหม่ที่มีองค์ประกอบและฟังก์ชันที่ต้องการ โปรดทราบว่าแบบฟอร์มนี้เป็นแบบฟอร์มใหม่ ไม่ใช่ส่วนขยาย ตั้งชื่อแบบฟอร์ม `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail` โดยที่: 

    - `<ExtensionPrefix>` ระบุโซลูชันของคุณ โดยทั่วไปใช้ชื่อบริษัทของคุณ
    - `<FormName>` เป้นชื่อเฉพาะสำหรับแบบฟอร์ม

1. สร้างรายการเมนูที่ชื่อ `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`
1. สร้างส่วนขยายที่ชื่อ `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` โดยที่วิธีการ `getDetailsMenuItemList` จะถูกขยายโดยเพิ่มรายการเมนูใหม่ลงในรายการ

เมื่อคุณเสร็จสิ้นแล้ว มุมมองรายละเอียดใหม่จะแสดงรายการโดยอัตโนมัติในกล่องชุดคอมโบ **มุมมองรายละเอียด** ในหน้า **แท็บการออกแบบ** ใน Supply Chain Management คุณ (หรือผู้ดูแลระบบ หรือผู้จัดการฝ่ายผลิต) สามารถเพิ่มไปยังแท็บใหม่หรือแท็บที่มีอยู่แล้วได้อย่างง่ายดาย เช่นเดียวกับที่คุณสามารถเพิ่มมุมมองรายละเอียดมาตรฐานได้ สำหรับคำแนะนำ ให้ดูที่ [ออกแบบอินเทอร์เฟสการดำเนินการผลิต](production-floor-execution-tabs.md)

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>เพิ่มแป้นพิมพ์ตัวเลขให้กับแบบฟอร์มหรือกล่องโต้ตอบ

ตัวอย่างต่อไปนี้แสดงวิธีการเพิ่มแป้นพิมพ์ตัวเลขให้กับแบบฟอร์ม

1. จํานวนตัวควบคุมแป้นพิมพ์ตัวเลขซึ่งแต่ละแบบฟอร์มมี ต้องเท่ากับจํานวนแป้นพิมพ์ตัวเลขในแบบฟอร์มนั้น

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. ตั้งค่าลักษณะการทำงานของตัวควบคุมแป้นพิมพ์ตัวเลข และเชื่อมต่อตัวควบคุมแป้นพิมพ์ตัวเลขกับส่วนของฟอร์มแป้นพิมพ์ตัวเลข

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>ใช้แป้นพิมพ์ตัวเลขเป็นกล่องโต้ตอบป๊อปอัพ

ตัวอย่างต่อไปนี้แสดงวิธีหนึ่งในการตั้งค่าตัวควบคุมแป้นพิมพ์ตัวเลขในกล่องโต้ตอบป๊อปอัพ

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

ตัวอย่างต่อไปนี้แสดงวิธีหนึ่งในการเรียกตัวควบคุมแป้นพิมพ์ตัวเลขในกล่องโต้ตอบป๊อปอัพ

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ออกแบบอินเทอร์เฟสการดำเนินการผลิต](production-floor-execution-styles.md)
- [ออกแบบอินเทอร์เฟสการดำเนินการผลิต](production-floor-execution-tabs.md)
