# liying2209010072
import random  
# 定义虚拟信息的函数  
def generate_virtual_info():  
    # 虚拟联系方式  
    phone = '138' + ''.join(random.choices('0123456789', k=8))  
    email = f'liying{random.randint(1000, 9999)}@example.com'  
      
    # 虚拟求职意向  
    job_types = ['全职', '兼职', '实习']  
    job_roles = ['软件工程师', '数据分析师', '产品经理']  
    cities = ['北京', '上海', '广州', '深圳']  
    job_type = random.choice(job_types)  
    job_role = random.choice(job_roles)  
    city = random.choice(cities)  
      
    # 虚拟教育背景  
    universities = ['北京大学', '清华大学', '复旦大学', '上海交通大学']  
    majors = ['计算机科学与技术', '软件工程', '数据分析', '人工智能']  
    university = random.choice(universities)  
    major = random.choice(majors)  
      
    # 虚拟工作经历  
    companies = ['腾讯科技有限公司', '阿里巴巴集团', '百度公司', '字节跳动']  
    positions = ['软件工程师', '数据分析师', '产品经理', '项目经理']  
    company = random.choice(companies)  
    position = random.choice(positions)  
      
    # 虚拟技能清单  
    programming_languages = ['Python', 'Java', 'C++', 'JavaScript']  
    frameworks = ['React', 'Vue', 'Spring Boot', 'Django']  
    databases = ['MySQL', 'MongoDB', 'PostgreSQL', 'Redis']  
      
    # 虚拟自我评价  
    self_evaluations = [  
        '具备扎实的编程基础和良好的算法能力，熟悉多种编程语言和框架。',  
        '拥有丰富的项目经验，能够独立完成需求分析、设计和开发。',  
        '具备良好的沟通能力和团队合作精神，能够与不同背景的人有效协作。',  
        '对新技术保持高度敏感，喜欢尝试和探索新的技术领域。'  
    ]  
      
    return {  
        'phone': phone,  
        'email': email,  
        'job_type': job_type,  
        'job_role': job_role,  
        'city': city,  
        'university': university,  
        'major': major,  
        'company': company,  
        'position': position,  
        'programming_languages': programming_languages,  
        'frameworks': frameworks,  
        'databases': databases,  
        'self_evaluation': random.choice(self_evaluations)  
    }  
  
# 生成虚拟信息  
virtual_info = generate_virtual_info()  
  
# 创建README.md内容  
readme_content = f'''  
# 李颖的求职简历  
  
## 个人信息  
- 姓名：李颖  
- 学号：2209010072  
- 电话：{virtual_info['phone']}  
- 邮箱：{virtual_info['email']}  
  
## 求职意向  
- 求职类型：{virtual_info['job_type']}  
- 意向岗位：{virtual_info['job_role']}  
- 意向城市：{virtual_info['city']}  
  
## 教育背景  
- **{virtual_info['university']}** | **{virtual_info['major']}** | 本科  
  
## 工作经历  
- **{virtual_info['company']}** | **{virtual_info['position']}**   
  - 负责项目需求分析、设计和开发，确保项目按时交付。  
  - 参与代码审查，提高代码质量和可维护性。  
  - 与团队成员紧密合作，解决项目中的技术难题。  
  
## 技能清单  
- **编程语言**：{', '.join(virtual_info['programming_languages'][:random.randint(1, 4)])}  
- **框架**：{', '.join(virtual_info['frameworks'][:random.randint(1, 4)])}  
- **数据库**：{', '.join(virtual_info['databases'][:random.randint(1, 4)])}  
  
## 自我评价  
{virtual_info['self_evaluation']}  
'''  
  
# 打印README.md内容  
print(readme_content)
