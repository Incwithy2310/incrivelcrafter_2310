local _="Instance";local a="ScreenGui";local b="Frame";local c="TextButton";local d="UserInputService";local e="Mouse";local f="TextLabel";local g=game:GetService("Players").LocalPlayer;local h=game:GetService("TweenService");local i=game:GetService("UserInputService");local j=game:GetService("RunService");local k=game:GetService("Players").LocalPlayer.Character;local l=game:GetService("Workspace").CurrentCamera;local m=game:GetService("Players").LocalPlayer:GetMouse();local n=Vector2.new;local o=UDim2.new;local p=Color3.fromRGB;local q=game:GetService("TweenService");local r=Vector2.new;local s=Vector2.new(0,0);local t=Vector2.new(200,50)

local u=Instance.new(_);u.Name="x";u.Parent=g:WaitForChild("PlayerGui")
local v=Instance.new(b);v.Size=o(0,300,0,100);v.Position=o(0,200,0,200);v.BackgroundColor3=p(169,169,169);v.Parent=u;
local w=Instance.new(c);w.Size=o(0,150,0,50);w.Position=o(0.5,-75,0.5,-25);w.BackgroundColor3=p(255,0,0);w.Text="bored button";w.Parent=v;
local x=game.Players.LocalPlayer:GetMouse();local y=nil;
v.InputBegan:Connect(function(z,a)if a then return end;if z.UserInputType==Enum.UserInputType.MouseButton1 then
    local b,c=x.X,x.Y;local d=game:GetService("RunService").Heartbeat:Connect(function()v.Position=o(0,math.clamp(x.X-b,0,l.ViewportSize.X-300),0,math.clamp(x.Y-c,0,l.ViewportSize.Y-100))end)
    z.InputEnded:Connect(function()d:Disconnect()end)end end);

w.MouseButton1Click:Connect(function()
    game:GetService("Players").LocalPlayer.Character:BreakJoints()end)
   
