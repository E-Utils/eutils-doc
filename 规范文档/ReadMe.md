# 一、开发规范
    step 1: 方法设计文档编辑并检视（文档主要包括函数以及参数命名，函数预实现的功能等），通过检视后文档入库；
    step 2: 方法开发；
    step 3: 代码检视;
    step 4: 测试用例补充;
    step 5: 方法的使用文档编写并入库，同时更新wiki上方法的使用文档;

# 二、分支规范
    1. master
       主分支，所有分支代码基于该分支拉取;
    2. trunk
       主干分支，当开发完成并通过测试后，开发人员将代码合并到trunk，并基于该分支拉取release分支发布，发布上线后将trunk合并到master；
    3. dev
       开发合并分支，当开发人员完成开发并通过自测后，统一合并到dev，通过dev去测试所有的代码；
    4. release
       发布分支，发布时基于trunk拉取release分支，分支命名release_v + version(eg:release_v1.0.0);
    5. develop branch
       个人开发分支，命名方式：name_v + version(eg: yhm_v1.0.0)，所有个人分支基于master拉取;

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





