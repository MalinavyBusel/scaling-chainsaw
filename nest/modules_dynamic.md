Мы можем дать классу модуля возможность конфигурации, передавая в него параметры с помощью ф-й register и forRoot, когда мы его импортируем.
Эти методы возвращают динамический модуль - модуль, который создан в рантайме.

register возвращает объект с обязательным полем module, в которром значение - класс-владелец метода register. Параметры, переданные в register,
затем можно будет получить внутри сервисов этого модуля при помощи di неста.

```
@Module({
  imports: [ConfigModule.register({ folder: './config' })],
    controllers: [AppController],
    providers: [AppService],
})
export class ConfigModule {
    static register(options: Record<string, any>): DynamicModule {
        return {
            module: ConfigModule,
            providers: [
                {
                    provide: 'CONFIG_OPTIONS',
                    useValue: options,
                },
                ConfigService,
            ],
            exports: [ConfigService],
        };
    }
}
```


Варианты названий метода:
- forRoot - используем много где
- register - настраиваем и используем только в конкретном модуле
- forFeature - хотим использовать конфиг forRoot-a, но нужно кое-что сменить


Для того, чтобы не париться с настройкой, можно использовать встроенный ConfigurableModuleBuilder. 
