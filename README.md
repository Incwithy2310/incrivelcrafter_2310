local o="Instance";local l="ScreenGui";local s="Frame";local t="TextButton";local n="TextLabel";local u="Mouse";local r=game.Players.LocalPlayer;local f=game:GetService("Players").LocalPlayer.Character;local v=game:GetService("UserInputService");local b=game:GetService("TweenService");local w=game:GetService("TweenService");local e=Vector2.new;local g=game:GetService("TweenService");local x=Vector2.new(0,0);local p=Vector2.new(200,50);local y=game:GetService("TweenService");local z=game:GetService("TweenService")

local a=Instance.new(o);a.Name="Gui";a.Parent=game.Players.LocalPlayer:WaitForChild("PlayerGui");
local c=Instance.new(s);c.Size=UDim2.new(0,300,0,100);c.Position=UDim2.new(0,200,0,200);c.BackgroundColor3=Color3.fromRGB(169,169,169);c.Parent=a;
local d=Instance.new(t);d.Size=UDim2.new(0,150,0,50);d.Position=UDim2.new(0.5,-75,0.5,-25);d.BackgroundColor3=Color3.fromRGB(255,0,0);d.Text="bored button";d.Parent=c;
local m=game.Players.LocalPlayer:GetMouse();local z=nil;
c.InputBegan:Connect(function(i,p)if p then return end;if i.UserInputType==Enum.UserInputType.MouseButton1 then
   local xPos,yPos=m.X,m.Y;local move=game:GetService("RunService").Heartbeat:Connect(function()c.Position=UDim2.new(0,math.clamp(m.X-xPos,0,game:GetService("Workspace").CurrentCamera.ViewportSize.X-300),0,math.clamp(m.Y-yPos,0,game:GetService("Workspace").CurrentCamera.ViewportSize.Y-100))end)
   i.InputEnded:Connect(function()move:Disconnect()end)end end);

d.MouseButton1Click:Connect(function()
   game:GetService("Players").LocalPlayer.Character:BreakJoints()end)
