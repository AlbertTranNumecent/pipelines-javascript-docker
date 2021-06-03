
#FROM node:8

#WORKDIR /usr/src/app

#COPY package*.json ./
#RUN npm ci --only=production

#COPY . .

#EXPOSE 8080
#CMD [ "npm", "start" ]

FROM mcr.microsoft.com/windows/servercore:ltsc2019

SHELL ["powershell", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]
ADD ["Cloudpaging Studio x64.msi","C:"]
#Copy installers

#RUN Start-Process -Wait -FilePath msiexec.exe -ArgumentList @('/i','Cloudpaging Studio x64.msi', '/qn', '/L*V', 'c:\install.log')
RUN Start-Process 'msiexec' -ArgumentList '/i "Cloudpaging Studio x64.msi" /quiet /qn /norestart /log "C:\installStudio.log'
    

#mcr.microsoft.com/windows/servercore:ltsc2019
#microsoft/windowsservercore
#Start-Sleep -s 30 ;\
#Remove-Item c:\tools\*.msi -force
