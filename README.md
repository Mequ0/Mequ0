```typescript

Mequ = {}

function Mequ:self()
    local obj = {
        name = "Tomek",
        dateOfBirth = "2008-10-30"
    }
    setmetatable(obj, self)
    self.__index = self
    return obj
end

function Mequ:languages()
    return {
        ['Polish'] = 'Native',
        ['English'] = 'Fluent',
        ['German'] = 'Beginner'
    }
end

function Mequ:education()
    return {
        ['2020-now'] = 'Learning Lua'
    }
end

function Mequ:projects()
    return {
        'Small RolePlay servers in FiveM',
        'One larger RolePlay server'
    }
end

function Mequ:printAll()
    print("Name: " .. self.name)
    print("Date of Birth: " .. self.dateOfBirth)

    
    print("Languages:")
    for language, level in pairs(self:languages()) do
        print("  " .. language .. ": " .. level)
    end
    
    print("Education:")
    for year, edu in pairs(self:education()) do
        print("  " .. year .. ": " .. edu)
    end
    
    print("Projects:")
    for _, project in ipairs(self:projects()) do
        print("  - " .. project)
    end

end

local mequ = Mequ:self()
mequ:printAll()


``````
###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Mequ0&hide_title=true&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=aura_dark&locale=en&hide_border=true" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=Mequ0&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=aura_dark&hide_border=true" height="150" alt="languages graph"  />
</div>

###

<br clear="both">

<img src="https://raw.githubusercontent.com/Mequ0/Mequ0/output/snake.svg" alt="Snake animation" />

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/lua/lua-original.svg" height="30" alt="lua logo"  />
</div>

###
