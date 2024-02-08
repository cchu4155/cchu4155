- 👋 Hi, I’m @cchu4155
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
cchu4155/cchu4155 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
this is my first program



# def use_logging(func):
#
#     def wrapper(name):
#         print("%s is running" % func.__name__)
#         return func(name)
#     return wrapper
#
# @use_logging
# #foo=use_logging(foo)
# #主业务函数带参数
# #装饰器带参数
# def foo(f1):
#     print(f"i am foo     {f1}")
#
# foo("测试业务函数带参数")



def log(text):
    def decorator(func):
        def wrapper(*args, **kw):
            print('%s %s():' % (text, func.__name__))
            return func(*args, **kw)
        return wrapper
    return decorator


@log("3123")
def foo():
    print("i am foo")

foo()

