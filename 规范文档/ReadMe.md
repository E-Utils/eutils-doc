# 一、开发规范
    step 1: 方法设计文档编写并检视（文档主要包括函数以及参数命名，函数预实现的功能并举例等），通过检视后文档入库（https://github.com/E-Utils/documents/tree/master/%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3）；
    step 2: 方法开发；
        自行拉取分支开发，也可约定在同一分支上开发，命名严格按照分支规范
    step 3: 代码检视;
    step 4: 测试用例补充;
    step 5: 方法的使用文档编写并入库，同时更新wiki上方法的使用文档;

# 二、分支规范
    1. master
       主分支，与线上代码保持一致，不能被修改，当一个版本发布后，才会被合入新版本代码；
    2. trunk
       主干分支，继承自master，当开发完成并通过测试后，开发人员将代码合并到trunk，并基于该分支拉取release分支发布，发布上线后将trunk合并到master；
    3. develop
       项目迭代分支，继承自master，新迭代开始时，从master拉取develop分支作为当前迭代的迭代分支，基于该分支开发人员去拉取个人feature分支，当开发人员完成开发并通过自测后，统一合并到develop，通过develop去测试所有的代码，develop命名`develop_v${version}`(eg: develop_v1.0.0)；
    4. release
       发布分支，发布时基于trunk拉取release分支，分支命名`release_v${version}`(eg:release_v1.0.0);
    5. feature
       个人开发分支，命名方式：`feature_v${version}_${name}`(eg: feature_v1.0.0_yhm)，所有个人分支基于当前迭代的develop分支拉取;

# 三、注释规范
    /**
     * What is the function used to do?;
     * 
     * @since version(eg: 1.0.0);
     * @category math;
     * @author name + id(eg: yhm1694);
     * @param {string} x The arguement of the function;
     * @return {string} The returns of the function;
     * @create_date The create date of the function(eg: 2018/09/09);
     * @modify_date The last modify date of the function(eg: 2018/09/10);
     * @example
     *
     * add(1, 2)
     * // => 3 
     * /

# 四、禅道任务创建规范
    ［任务类型］－ 任务名称；
     eg:
        ［开发］－ dateFormat日期格式化输出方法开发；
        ［测试］－ dateFormat日期格式化输出单元测试用例编写；
        ［文档］－ dateFormat日期格式化输出函数使用文档编辑;
        ［基设］－ 脚手架代码覆盖率检测功能新增；
        ［其他］－ 任务细分；

# 五、git提交日志规范
    git commit 信息规范：
    {type} － {event}
    eg:
        dev - 开发hello方法，返回hello字符串;
        test - 补充hello方法测试用例;
        doc - 补充hello方法使用文档;
        bugFix - hello方法返回值错误bug修复; 




