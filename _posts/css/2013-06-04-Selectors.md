---
layout: post
category : css
title: Selectors选择器
---

    var tip = ["指定元素名称", "属性中包含", "属性开始", "属性结束", "属性等于",
            "html部分", "元素内容为空白", "锚",
            "子元素", "兄弟元素", "第一个", "最后一个元素", "第2个", "倒数第2个",
            "奇数", "偶数", "类型一致的奇数", "类型一致的偶数",
            "从第3个算起，   每隔2个（包含第2个）", "只有一个子元素",
            "可用状态", "不可用状态", "只读", "非只读", "选取状", "非选取状态", "一半状态", "不包含"
            ];

    var selectors = ["ol",
                    "[title*=abc]", "[title^=abc]", "[title$=abc]", "[title=abc]",
                    ":root",
                    ":empty",
                    ":target",
                    "ol li",
                    "ol~p",
                    "ol li:first-child", "ol li:last-child", "ol li:nth-child(2)", "ol li:nth-last-child(2)",
                    "ol li:nth-child(odd)", "ol li:nth-child(even)", "ol li:nth-of-type(odd)", "ol li:nth-of-type(even)",
                    "li:nth-child(2n+3)",
                    "ol li:only-child",
                    ":enabled", ":disabled", ":read-only", ":read-write",
                    ":default", ":checked", ":indeterminate",
                    "ol li:not(:first-child)"
                    ];