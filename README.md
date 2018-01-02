# Java 代码质量检查
## FindBugs
收集整理了部分个人觉得相对重要的一些检查项。

## Checkstyle
主要整合了 Google 的 checkstyle 规则和华为的 checkstyle 规则。并添加了部分个人觉得也有必要的规则，

个人增加规则：

- 检查代码中不允许使用 `System.out.println();`。
- 检查代码中不允许使用 `e.printStackTrace();`。
- 代码缩进统一使用`空格`而不是 `Tab` 制表符。
- 增加跳过检查的关键字 `CSOFF`、`CSON`（跳过所有类型），`CSOFF: xxx|xxx`、`CSON: xxx|xxx`（跳过指定的多个类型）。相关参考： http://checkstyle.sourceforge.net/config_filters.html#SuppressionCommentFilter

Google Checkstyle: https://github.com/checkstyle/checkstyle/blob/master/src/main/resources/google_checks.xml

华为 Checkstyle: https://gist.github.com/ownwell/c32878440216f1866842

## PMD
根据 PMD 官方 6.0.0 版本整理 https://pmd.github.io/pmd-6.0.0/pmd_rules_java.html

- `pmd-ruleset.xml` 可兼容 IDEA 插件 PMDPlugin v1.8.3 版本。
- `pmd-ruleset-supplement.xml` 为根据 PMD 官方 6.0.0 版本扩展的规则，在 PMDPlugin 中暂时不能支持（应该是 PMDPlugin 插件使用的 PMD 包的版本关系），但可通过 Maven 添加（在 Maven 中可以自定 PMD 包的版本）。