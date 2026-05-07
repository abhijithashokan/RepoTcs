# Restaurant Menu Application

Food Menu with Details

This is tech food company which displays food items with price




exact config for your pod <configuration>

    <appender name="STDOUT"
              class="ch.qos.logback.core.ConsoleAppender">

        <encoder>
            <pattern>
                %d{yyyy-MM-dd HH:mm:ss.SSS} %-5level [%thread] %logger{36} - %msg%n
            </pattern>
        </encoder>
    </appender>

    <appender name="ASYNC_STDOUT"
              class="ch.qos.logback.classic.AsyncAppender">

        <!-- Queue capacity -->
        <queueSize>50000</queueSize>

        <!-- Never block app threads -->
        <neverBlock>true</neverBlock>

        <!-- Keep all INFO/WARN/ERROR -->
        <discardingThreshold>0</discardingThreshold>

        <!-- Caller data expensive -->
        <includeCallerData>false</includeCallerData>

        <appender-ref ref="STDOUT"/>
    </appender>

    <root level="INFO">
        <appender-ref ref="ASYNC_STDOUT"/>
    </root>

</configuration>
