function notify(text, duration)
    local SynergyNotifications = Instance.new("ScreenGui")


    SynergyNotifications.Name = "SynergyNotifications"
    SynergyNotifications.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
    SynergyNotifications.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
    
    local SynergyX = Instance.new("Frame")
    SynergyX.Name = "SynergyX"
    SynergyX.Parent = SynergyNotifications
    SynergyX.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    SynergyX.BackgroundTransparency = 1
    SynergyX.Position = UDim2.new(0.706528306, 0, 0.00117647054, 0)
    SynergyX.Size = UDim2.new(0.293471634, 0, 0.998823524, 0)
    
    local Notify = Instance.new("Frame")
    Notify.Name = "Notify"
    Notify.Parent = SynergyX
    Notify.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
    Notify.Position = UDim2.new(0.00207901001, 0, 0.874635339, 0)
    Notify.Size = UDim2.new(0.99792099, 0, 0.0647820979, 0)
    
    local TextLabel = Instance.new("TextLabel")
    TextLabel.Parent = Notify
    TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    TextLabel.BackgroundTransparency = 1.000
    TextLabel.Position = UDim2.new(0.141666681, 0, 0.0219620466, 0)
    TextLabel.Size = UDim2.new(0.875, 0, 0.909090936, 0)
    TextLabel.Font = Enum.Font.SourceSans
    TextLabel.Text = text
    TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
    TextLabel.TextScaled = true
    TextLabel.TextSize = 35.000
    TextLabel.TextWrapped = true
    TextLabel.TextXAlignment = Enum.TextXAlignment.Left
    
    local UITextSizeConstraint = Instance.new("UITextSizeConstraint")
    UITextSizeConstraint.Parent = TextLabel
    UITextSizeConstraint.MaxTextSize = 35
    
    local ImageLabel = Instance.new("ImageLabel")
    ImageLabel.Parent = Notify
    ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    ImageLabel.BackgroundTransparency = 1.000
    ImageLabel.Position = UDim2.new(-0.0291666668, 0, -0.421672463, 0)
    ImageLabel.Size = UDim2.new(0.208333328, 0, 1.81818187, 0)
    ImageLabel.Image = "http://www.roblox.com/asset/?id=13365902191"
    
    local UIGridLayout = Instance.new("UIGridLayout")
    UIGridLayout.Parent = SynergyX
    UIGridLayout.SortOrder = Enum.SortOrder.LayoutOrder
    UIGridLayout.VerticalAlignment = Enum.VerticalAlignment.Bottom
    UIGridLayout.CellSize = UDim2.new(0, 480, 0, 55)
    wait(duration)
    SynergyNotifications:Destroy()
end

if shared.SynergyXLibrary then
    notify("Synergy Library Already Injected", 2)
    else
    shared.SynergyXLibrary = true
    local library = {}
    
    function library:Add(name)
    
        local Loader = Instance.new("ScreenGui")	
    
    
        Loader.Name = "Loader"
        Loader.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
        Loader.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
        Loader.ResetOnSpawn = false
    
        local MainContainer = Instance.new("Frame")
        MainContainer.Name = "MainContainer"
        MainContainer.Parent = Loader
        MainContainer.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        MainContainer.Position = UDim2.new(0.278471708, 0, 0.298823506, 0)
        MainContainer.Size = UDim2.new(0, 602, 0, 341)
        MainContainer.Active = true
        MainContainer.Draggable = true
    
        local TabList = Instance.new("Frame")
        TabList.Name = "TabList"
        TabList.Parent = MainContainer
        TabList.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
        TabList.BorderSizePixel = 0
        TabList.Size = UDim2.new(0, 128, 0, 341)
    
        local UIListLayout = Instance.new("UIListLayout")
        UIListLayout.Parent = TabList
        UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
        UIListLayout.Padding = UDim.new(0, 1)
    
        local HubName = Instance.new("TextLabel")
        HubName.Name = "HubName"
        HubName.Parent = TabList
        HubName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        HubName.BackgroundTransparency = 1.000
        HubName.BorderSizePixel = 0
        HubName.Position = UDim2.new(0.9375, 0, 0, 0)
        HubName.Size = UDim2.new(0, 126, 0, 33)
        HubName.Font = Enum.Font.SourceSans
        HubName.Text = name
        HubName.TextColor3 = Color3.fromRGB(255, 255, 255)
        HubName.TextSize = 21.000
    
        local Tab = Instance.new("TextButton")
        Tab.Name = "Tab"
        Tab.Parent = TabList
        Tab.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        Tab.BackgroundTransparency = 1.000
        Tab.Position = UDim2.new(0.984375, 0, 0.0263929628, 0)
        Tab.Size = UDim2.new(0, 126, 0, 33)
        Tab.Font = Enum.Font.SourceSans
        Tab.Text = "Tab1"
        Tab.TextColor3 = Color3.fromRGB(255, 255, 255)
        Tab.TextSize = 21.000
        Tab.TextWrapped = true
    
        local CloseButton = Instance.new("TextButton")
        CloseButton.Name = "CloseButton"
        CloseButton.Parent = MainContainer
        CloseButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        CloseButton.BackgroundTransparency = 1.000
        CloseButton.Position = UDim2.new(0.943521619, 0, 0, 0)
        CloseButton.Size = UDim2.new(0, 34, 0, 26)
        CloseButton.Font = Enum.Font.SourceSans
        CloseButton.Text = "X"
        CloseButton.TextColor3 = Color3.fromRGB(255, 255, 255)
        CloseButton.TextScaled = true
        CloseButton.TextSize = 14.000
        CloseButton.TextWrapped = true
    
        local shadowHolder = Instance.new("Frame")
        shadowHolder.Name = "shadowHolder"
        shadowHolder.Parent = MainContainer
        shadowHolder.BackgroundTransparency = 1.000
        shadowHolder.Position = UDim2.new(-0.0149501152, 0, -0.0263930075, 0)
        shadowHolder.Size = UDim2.new(1.02491689, 0, 1.05865109, 0)
        shadowHolder.ZIndex = 0
    
        local umbraShadow = Instance.new("ImageLabel")
        umbraShadow.Name = "umbraShadow"
        umbraShadow.Parent = shadowHolder
        umbraShadow.AnchorPoint = Vector2.new(0.5, 0.5)
        umbraShadow.BackgroundTransparency = 1.000
        umbraShadow.Position = UDim2.new(0.5, 0, 0.5, 2)
        umbraShadow.Size = UDim2.new(1, 4, 1, 4)
        umbraShadow.ZIndex = 0
        umbraShadow.Image = "rbxassetid://1316045217"
        umbraShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
        umbraShadow.ImageTransparency = 0.860
        umbraShadow.ScaleType = Enum.ScaleType.Slice
        umbraShadow.SliceCenter = Rect.new(10, 10, 118, 118)
    
        local penumbraShadow = Instance.new("ImageLabel")
        penumbraShadow.Name = "penumbraShadow"
        penumbraShadow.Parent = shadowHolder
        penumbraShadow.AnchorPoint = Vector2.new(0.5, 0.5)
        penumbraShadow.BackgroundTransparency = 1.000
        penumbraShadow.Position = UDim2.new(0.5, 0, 0.5, 2)
        penumbraShadow.Size = UDim2.new(1, 4, 1, 4)
        penumbraShadow.ZIndex = 0
        penumbraShadow.Image = "rbxassetid://1316045217"
        penumbraShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
        penumbraShadow.ImageTransparency = 0.880
        penumbraShadow.ScaleType = Enum.ScaleType.Slice
        penumbraShadow.SliceCenter = Rect.new(10, 10, 118, 118)
    
        local ambientShadow = Instance.new("ImageLabel")
        ambientShadow.Name = "ambientShadow"
        ambientShadow.Parent = shadowHolder
        ambientShadow.AnchorPoint = Vector2.new(0.5, 0.5)
        ambientShadow.BackgroundTransparency = 1.000
        ambientShadow.Position = UDim2.new(0.5, 0, 0.5, 2)
        ambientShadow.Size = UDim2.new(1, 4, 1, 4)
        ambientShadow.ZIndex = 0
        ambientShadow.Image = "rbxassetid://1316045217"
        ambientShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
        ambientShadow.ImageTransparency = 0.880
        ambientShadow.ScaleType = Enum.ScaleType.Slice
        ambientShadow.SliceCenter = Rect.new(10, 10, 118, 118)
    
        local Tab1 = Instance.new("ScrollingFrame")
        Tab1.Name = "Tab1"
        Tab1.Parent = MainContainer
        Tab1.Active = true
        Tab1.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        Tab1.BackgroundTransparency = 1.000
        Tab1.BorderColor3 = Color3.fromRGB(20, 20, 20)
        Tab1.Position = UDim2.new(0.222289026, 0, 0.0762463361, 0)
        Tab1.Size = UDim2.new(0, 469, 0, 314)
    
        local UIListLayout_2 = Instance.new("UIListLayout")
        UIListLayout_2.Parent = Tab1
        UIListLayout_2.SortOrder = Enum.SortOrder.LayoutOrder
        UIListLayout_2.Padding = UDim.new(0, 4)
    
        local function EDHOEX_fake_script() -- CloseButton.LocalScript 
            local script = Instance.new('LocalScript', CloseButton)
    
            script.Parent.MouseButton1Down:Connect(function()
                shared.SynergyXLibrary = false
                script.Parent.Parent.Visible = false
            end)
        end
        coroutine.wrap(EDHOEX_fake_script)()
    
    
        local SynergyLibrary = {}
    
        function SynergyLibrary:CreateButton(text, callback)
            local callback = callback or function() end
    
            local ButtonFrame = Instance.new("Frame")
            ButtonFrame.Name = "ButtonFrame"
            ButtonFrame.Parent = Tab1
            ButtonFrame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
            ButtonFrame.Position = UDim2.new(0.0209643599, 0, 0.00825519953, 0)
            ButtonFrame.Size = UDim2.new(0, 456, 0, 37)
    
            local UICorner_2 = Instance.new("UICorner")
            UICorner_2.CornerRadius = UDim.new(0, 6)
            UICorner_2.Parent = ButtonFrame
    
            local Button = Instance.new("TextLabel")
            Button.Name = "Button"
            Button.Parent = ButtonFrame
            Button.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Button.BackgroundTransparency = 1.000
            Button.Position = UDim2.new(0.0933683962, 0, -0.0190272983, 0)
            Button.Size = UDim2.new(0, 413, 0, 37)
            Button.Font = Enum.Font.SourceSans
            Button.Text = text
            Button.TextColor3 = Color3.fromRGB(255, 255, 255)
            Button.TextSize = 21.000
            Button.TextXAlignment = Enum.TextXAlignment.Left
    
            local ClickButton = Instance.new("ImageLabel")
            ClickButton.Name = "Click Button"
            ClickButton.Parent = ButtonFrame
            ClickButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            ClickButton.BackgroundTransparency = 1.000
            ClickButton.Size = UDim2.new(0, 36, 0, 34)
            ClickButton.Image = "rbxassetid://12804017021"
    
            local ClickFeature = Instance.new("TextButton")
            ClickFeature.Name = "ClickFeature"
            ClickFeature.Parent = ButtonFrame
            ClickFeature.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            ClickFeature.BackgroundTransparency = 1.000
            ClickFeature.Size = UDim2.new(0, 452, 0, 35)
            ClickFeature.Font = Enum.Font.SourceSans
            ClickFeature.Text = ""
            ClickFeature.TextColor3 = Color3.fromRGB(0, 0, 0)
            ClickFeature.TextSize = 14.000
            ClickFeature.TextTransparency = 1.000
            ClickFeature.MouseButton1Down:Connect(function()
                pcall(callback)
            end)
        end
    
        function SynergyLibrary:CreateLabel(text)
    
            local LabelFrame = Instance.new("Frame")
            LabelFrame.Name = "LabelFrame"
            LabelFrame.Parent = Tab1
            LabelFrame.BackgroundColor3 = Color3.fromRGB(209, 0, 3)
            LabelFrame.Position = UDim2.new(0.0209643599, 0, 0.00825519953, 0)
            LabelFrame.Size = UDim2.new(0, 456, 0, 37)
    
            local UICorner = Instance.new("UICorner")
            UICorner.CornerRadius = UDim.new(0, 6)
            UICorner.Parent = LabelFrame
    
            local Label = Instance.new("TextLabel")
            Label.Name = "Label"
            Label.Parent = LabelFrame
            Label.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Label.BackgroundTransparency = 1.000
            Label.Position = UDim2.new(0.0122280456, 0, 0.00799972937, 0)
            Label.Size = UDim2.new(0, 449, 0, 37)
            Label.Font = Enum.Font.SourceSans
            Label.Text = text
            Label.TextColor3 = Color3.fromRGB(255, 255, 255)
            Label.TextSize = 21.000
            Label.TextXAlignment = Enum.TextXAlignment.Left
    
        end
    
        function SynergyLibrary:CreateToggle(text, callback)
            local actions = {}
            local enabled = false
    
            text = text or "New Toggle"
            callback = callback or function() end
    
            local ToggleFrame = Instance.new("Frame")
            ToggleFrame.Name = "ToggleFrame"
            ToggleFrame.Parent = Tab1
            ToggleFrame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
            ToggleFrame.Position = UDim2.new(0.0209643599, 0, 0.00825519953, 0)
            ToggleFrame.Size = UDim2.new(0, 456, 0, 37)
    
            local UICorner_3 = Instance.new("UICorner")
            UICorner_3.CornerRadius = UDim.new(0, 6)
            UICorner_3.Parent = ToggleFrame
    
            local Button_2 = Instance.new("TextLabel")
            Button_2.Name = "Button"
            Button_2.Parent = ToggleFrame
            Button_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Button_2.BackgroundTransparency = 1.000
            Button_2.Position = UDim2.new(0.0933683962, 0, -0.0190272983, 0)
            Button_2.Size = UDim2.new(0, 413, 0, 37)
            Button_2.Font = Enum.Font.SourceSans
            Button_2.Text = text
            Button_2.TextColor3 = Color3.fromRGB(255, 255, 255)
            Button_2.TextSize = 21.000
            Button_2.TextXAlignment = Enum.TextXAlignment.Left
    
            local Toggle = Instance.new("TextButton")
            Toggle.Name = "Toggle"
            Toggle.Parent = ToggleFrame
            Toggle.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
            Toggle.BorderSizePixel = 0
            Toggle.Position = UDim2.new(0.00219298247, 0, 0.0540540516, 0)
            Toggle.Size = UDim2.new(0, 33, 0, 32)
            Toggle.Font = Enum.Font.SourceSans
            Toggle.Text = ""
            Toggle.TextColor3 = Color3.fromRGB(0, 0, 0)
            Toggle.TextSize = 14.000
            Toggle.TextTransparency = 1.000
    
            local UICorner_4 = Instance.new("UICorner")
            UICorner_4.CornerRadius = UDim.new(0, 20)
            UICorner_4.Parent = Toggle
    
            local function Fire()
                enabled = not enabled
                Toggle.Text = enabled and utf8.char(10003) or ""
                pcall(callback, enabled)
            end
    
            Toggle.MouseButton1Click:Connect(Fire)
    
        end
        function SynergyLibrary:CreateSlider(text, minvalue, maxvalue, callback)
    
    
            --Properties:
            local SlidersFrame = Instance.new("Frame")
            SlidersFrame.Name = "SlidersFrame"
            SlidersFrame.Parent = Tab1
            SlidersFrame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
            SlidersFrame.Position = UDim2.new(0.0209643599, 0, 0.00825519953, 0)
            SlidersFrame.Size = UDim2.new(0, 456, 0, 37)
            
            local UICorner_5 = Instance.new("UICorner")
            UICorner_5.CornerRadius = UDim.new(0, 6)
            UICorner_5.Parent = SlidersFrame
            
            local Sliders = Instance.new("TextLabel")
            Sliders.Name = "Sliders"
            Sliders.Parent = SlidersFrame
            Sliders.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Sliders.BackgroundTransparency = 1.000
            Sliders.Position = UDim2.new(0.0122280456, 0, -0.0190272983, 0)
            Sliders.Size = UDim2.new(0, 123, 0, 37)
            Sliders.Font = Enum.Font.SourceSans
            Sliders.Text = text
            Sliders.TextColor3 = Color3.fromRGB(255, 255, 255)
            Sliders.TextSize = 21.000
            Sliders.TextXAlignment = Enum.TextXAlignment.Left
            
            local Sliders_2 = Instance.new("TextButton")
            Sliders_2.Name = "Sliders"
            Sliders_2.Parent = SlidersFrame
            Sliders_2.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
            Sliders_2.BorderSizePixel = 0
            Sliders_2.Position = UDim2.new(0.309210569, 0, 0.270270288, 0)
            Sliders_2.Size = UDim2.new(0, 301, 0, 17)
            Sliders_2.Font = Enum.Font.SourceSans
            Sliders_2.Text = ""
            Sliders_2.TextColor3 = Color3.fromRGB(0, 0, 0)
            Sliders_2.TextSize = 14.000
            Sliders_2.TextTransparency = 1.000
            
            local UICorner_6 = Instance.new("UICorner")
            UICorner_6.CornerRadius = UDim.new(0, 5)
            UICorner_6.Parent = Sliders_2
            
            local SlidersUp = Instance.new("Frame")
            SlidersUp.Name = "SlidersUp"
            SlidersUp.Parent = Sliders_2
            SlidersUp.BackgroundColor3 = Color3.fromRGB(218, 0, 4)
            SlidersUp.Size = UDim2.new(0, 301, 0, 15)
            
            local UICorner_7 = Instance.new("UICorner")
            UICorner_7.CornerRadius = UDim.new(0, 5)
            UICorner_7.Parent = SlidersUp
            
            local SliderValue = Instance.new("TextLabel")
            SliderValue.Name = "SliderValue"
            SliderValue.Parent = SlidersFrame
            SliderValue.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            SliderValue.BackgroundTransparency = 1.000
            SliderValue.Position = UDim2.new(0.308280677, 0, 0.656648397, 0)
            SliderValue.Size = UDim2.new(0, 40, 0, 13)
            SliderValue.Font = Enum.Font.SourceSans
            SliderValue.Text = "Sliders"
            SliderValue.TextColor3 = Color3.fromRGB(255, 255, 255)
            SliderValue.TextSize = 20.000
            SliderValue.TextXAlignment = Enum.TextXAlignment.Left
    
            minvalue = minvalue or 0
            maxvalue = maxvalue or 100
    
    
            callback = callback or function() end
    
    
            local mouse = game.Players.LocalPlayer:GetMouse()
            local uis = game:GetService("UserInputService")
            local Value;
    
    
    
    
    
            Sliders_2.MouseButton1Down:Connect(function()
                Value = math.floor((((tonumber(maxvalue) - tonumber(minvalue)) / 318) * SlidersUp.AbsoluteSize.X) + tonumber(minvalue)) or 0
                pcall(function()
                    callback(Value)
                end)
                SlidersUp.Size = UDim2.new(0, math.clamp(mouse.X - SlidersUp.AbsolutePosition.X, 0, 301), 0, 17)
                moveconnection = mouse.Move:Connect(function()
                    SliderValue.Text = Value
                    Value = math.floor((((tonumber(maxvalue) - tonumber(minvalue)) / 301) * SlidersUp.AbsoluteSize.X) + tonumber(minvalue))
                    pcall(function()
                        callback(Value)
                    end)
                    SlidersUp.Size = UDim2.new(0, math.clamp(mouse.X - SlidersUp.AbsolutePosition.X, 0, 301), 0, 17)
                end)
                releaseconnection = uis.InputEnded:Connect(function(Mouse)
                    if Mouse.UserInputType == Enum.UserInputType.MouseButton1 then
                        Value = math.floor((((tonumber(maxvalue) - tonumber(minvalue)) / 301) * SlidersUp.AbsoluteSize.X) + tonumber(minvalue))
                        pcall(function()
                            callback(Value)
                        end)
                        SlidersUp.Size = UDim2.new(0, math.clamp(mouse.X - SlidersUp.AbsolutePosition.X, 0, 301), 0, 17)
                        moveconnection:Disconnect()
                        releaseconnection:Disconnect()
                    end
                end)
            end)
        end
        function SynergyLibrary:CreateNotify(text, duration)
            local SynergyNotifications = Instance.new("ScreenGui")
        
        
            SynergyNotifications.Name = "SynergyNotifications"
            SynergyNotifications.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
            SynergyNotifications.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
            
            local SynergyX = Instance.new("Frame")
            SynergyX.Name = "SynergyX"
            SynergyX.Parent = SynergyNotifications
            SynergyX.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            SynergyX.BackgroundTransparency = 1
            SynergyX.Position = UDim2.new(0.706528306, 0, 0.00117647054, 0)
            SynergyX.Size = UDim2.new(0.293471634, 0, 0.998823524, 0)
            
            local Notify = Instance.new("Frame")
            Notify.Name = "Notify"
            Notify.Parent = SynergyX
            Notify.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
            Notify.Position = UDim2.new(0.00207901001, 0, 0.874635339, 0)
            Notify.Size = UDim2.new(0.99792099, 0, 0.0647820979, 0)
            
            local TextLabel = Instance.new("TextLabel")
            TextLabel.Parent = Notify
            TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.BackgroundTransparency = 1.000
            TextLabel.Position = UDim2.new(0.141666681, 0, 0.0219620466, 0)
            TextLabel.Size = UDim2.new(0.875, 0, 0.909090936, 0)
            TextLabel.Font = Enum.Font.SourceSans
            TextLabel.Text = text
            TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.TextScaled = true
            TextLabel.TextSize = 35.000
            TextLabel.TextWrapped = true
            TextLabel.TextXAlignment = Enum.TextXAlignment.Left
            
            local UITextSizeConstraint = Instance.new("UITextSizeConstraint")
            UITextSizeConstraint.Parent = TextLabel
            UITextSizeConstraint.MaxTextSize = 35
            
            local ImageLabel = Instance.new("ImageLabel")
            ImageLabel.Parent = Notify
            ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            ImageLabel.BackgroundTransparency = 1.000
            ImageLabel.Position = UDim2.new(-0.0291666668, 0, -0.421672463, 0)
            ImageLabel.Size = UDim2.new(0.208333328, 0, 1.81818187, 0)
            ImageLabel.Image = "http://www.roblox.com/asset/?id=13365902191"
            
            local UIGridLayout = Instance.new("UIGridLayout")
            UIGridLayout.Parent = SynergyX
            UIGridLayout.SortOrder = Enum.SortOrder.LayoutOrder
            UIGridLayout.VerticalAlignment = Enum.VerticalAlignment.Bottom
            UIGridLayout.CellSize = UDim2.new(0, 480, 0, 55)
            wait(duration)
            SynergyNotifications:Destroy()
        end
        return SynergyLibrary
    end

    
